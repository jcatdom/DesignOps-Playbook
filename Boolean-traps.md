# Boolean-traps

Every time you have to define a prop you should think about how it adapts with other existant props and future possible features.

Ex: Imagine you having the following component
```js
const Article = ({title, subtitle, children}) => (
  <article>
    <h1>{title}</h1>
    {subtitle ? <h2>{subtitle}</h2> : null}
    {children}
  </article>
)

Article.propTypes = {
  title: PropTypes.string,
  subtitle: PropTypes.string,
  children: PropTypes.node
}
```
Your stakeholder defines you a new feature which aligns all the texts to the right.

Maybe the first solution could be:
```js
const Article = ({title, subtitle, children, hasTextAlignRight}) => {
  const styles = useMemo(
    () => ({...(hasTextAlignLeft === 'right' && {textAlign: 'right'})}
  ), [hasTextAlignRight])
  return (
    <article>
      <h1 styles={styles}>{title}</h1>
      {subtitle ? <h2 styles={styles}>{subtitle}</h2> : null}
      <Injector styles={styles}>{children}</Injector>
    </article>
  )
}

Article.propTypes = {
  title: PropTypes.string,
  subtitle: PropTypes.string,
  children: PropTypes.node,
  hasTextAlignRight: PropTypes.bool
}
```

Easy! You got it. Everything works. Everyone is impressed about your ReactJs capability. But... yeap, of course there is always a "but...".

Two weeks later, another stakeholder remembers that amazing component and its new requirements are similar to that one. Of course you don't remember the particularities an implementation you code 2 weeks ago. The stakeholder also thinks you are the right person to develop his new amazing feature because you made last one faster than anyone soo he schedules a meeting with you for next week. He said you "Don't worry, it's similar to the one you made in past. You'll see" 

When the meeting arrives, the stakeholder explains to you that what he needs for its new article is just to align all the copies to the center. You do not remember exactly the current code but, Its just another text-align, easy-peasy. You leave the meeting, assign the task to yourself and open your IDE to start coding this way, and...

```js
// Last commit. 2 weeks ago.
const Article = ({title, subtitle, children, hasTextAlignRight}) => {
  const styles = useMemo(
    () => ({...(hasTextAlignLeft === 'right' && {textAlign: 'right'})}
  ), [hasTextAlignRight])
  return (
    <article>
      <h1 styles={styles}>{title}</h1>
      {subtitle ? <h2 styles={styles}>{subtitle}</h2> : null}
      <Injector styles={styles}>{children}</Injector>
    </article>
  )
}

Article.propTypes = {
  title: PropTypes.string,
  subtitle: PropTypes.string,
  children: PropTypes.node,
  hasTextAlignRight: PropTypes.bool
}
```

What should we do now? Lets take the same strategy.

```js
const Article = ({title, subtitle, children, hasTextAlignRight, hasTextAlignCenter}) => {
  const styles = useMemo(
    () => ({
      ...(hasTextAlignRight && {textAlign: 'right'}),
      ...(hasTextAlignCenter && {textAlign: 'center'})
    }
  ), [hasTextAlignRight, hasTextAlignCenter])
  return (
    <article>
      <h1 styles={styles}>{title}</h1>
      {subtitle ? <h2 styles={styles}>{subtitle}</h2> : null}
      <Injector styles={styles}>{children}</Injector>
    </article>
  )
}

Article.propTypes = {
  title: PropTypes.string,
  subtitle: PropTypes.string,
  children: PropTypes.node,
  hasTextAlignRight: PropTypes.bool,
  hasTextAlignCenter: PropTypes.bool
}
```

Of course, it also works but, can you see some weird strategy on that code?

What if the stakeholder wants during this year align the article using:
- justify
- revert
- end
- start
- whatever.

Let's take a look at the final component:

```js
const Article = ({
  title,
  subtitle,
  children,
  hasTextAlignRight,
  hasTextAlignCenter,
  hasTextAlignJustify,
  hasTextAlignRevert,
  hasTextAlignEnd,
  hasTextAlignStart,
  hasTextAlignWhatever,
}) => {
  const styles = useMemo(
    () => ({
      ...(hasTextAlignRight && {textAlign: 'right'}),
      ...(hasTextAlignCenter && {textAlign: 'center'}),
      ...(hasTextAlignJustify && {textAlign: 'justify'}),
      ...(hasTextAlignRevert && {textAlign: 'revert'}),
      ...(hasTextAlignEnd && {textAlign: 'end'}),
      ...(hasTextAlignStart && {textAlign: 'start'}),
      ...(hasTextAlignWhatever && {textAlign: 'whatever'}),
    }
  ), [
    hasTextAlignRight,
    hasTextAlignCenter,
    hasTextAlignJustify,
    hasTextAlignRevert,
    hasTextAlignEnd,
    hasTextAlignStart,
    hasTextAlignWhatever
  ])
  return (
    <article>
      <h1 styles={styles}>{title}</h1>
      {subtitle ? <h2 styles={styles}>{subtitle}</h2> : null}
      <Injector styles={styles}>{children}</Injector>
    </article>
  )
}

Article.propTypes = {
  title: PropTypes.string,
  subtitle: PropTypes.string,
  children: PropTypes.node,
  hasTextAlignRight:  PropTypes.bool,
  hasTextAlignCenter:  PropTypes.bool,
  hasTextAlignJustify:  PropTypes.bool,
  hasTextAlignRevert:  PropTypes.bool,
  hasTextAlignEnd:  PropTypes.bool,
  hasTextAlignStart:  PropTypes.bool,
  hasTextAlignWhatever:  PropTypes.bool
}
```

Have you seen that? Amazing Pisa tower!

Have you noticed what is going to happen if the defined props combines some of that boolean hasTextAlignStuff prop? There is no way to imagine what will happen unless you open your Component code and check the prior sorting strategy.

Now, that code makes no sense, and you have to talk to your product owner in order to include a tech debt task to refactor that code during the next sprint. A better approach can be seen in the use of enums over booleans.

Finally, the Article becomes:

```js
const Article = ({title, subtitle, children, textAlign}) => {
  const styles = useMemo(
    () => ({...(textAlign && {textAlign})}
  ), [textAlign])
  return (
    <article>
      <h1 styles={styles}>{title}</h1>
      {subtitle ? <h2 styles={styles}>{subtitle}</h2> : null}
      <Injector styles={styles}>{children}</Injector>
    </article>
  )
}

Article.propTypes = {
  title: PropTypes.string,
  subtitle: PropTypes.string,
  children: PropTypes.node,
  textAlign:  PropTypes.oneOf(Object.values(TEXT_ALIGN))
}
```

But..., yeap, there is a "but..." also. Can you see that?

We removed all existent `hasTextAlignStuff` boolean props and the current component has no retro-compatibility. We have unfortunately sent tech debt to all people who are using that component. This is a disgusting situation which could be avoided at the very beginning.   

## Enums Over Booleans

This sad situation is very common and the only way to avoid it is ***"Thinking out of the box"***. Every time a feature or a solution of a task seems to be resolved via a boolean flag, there is a red flag 🚩.

In Chapter 3 of Robert C. Martin’s “The Clean Code,” there is this brilliant bit on Flag Arguments:
> Flag arguments are ugly. Passing a boolean into a function is a truly terrible practice. It immediately complicates the signature of the method, loudly proclaiming that this function does more than one thing. It does one thing if the flag is true and another if the flag is false! –– ***Robert C. Martin's** "The Clean Coder" Cap.3*

Your IDE/Code Editor of choice should pickup on this and provide the proper signature and auto-complete options. It will never collide combined with other flags because there is only one prop self enclosing all different text-align strategies.

## Booleans and Control Flow

I hate seeing booleans in my codebase, but one case where you just can’t get rid of them seems to be external control flow.

For example when you want to use a dynamic control flag to control boolean native tag attributes to disable an input, add a loading indicator, or control a modal. Usually, it looks like this:
```js
  <input disabled={disabled} />
  <button loading={loading} />
  <Modal isOpen={isOpen} />
```

Sometimes these tend to pile up:

```js
 <form loading="{loading}" disabled="{disabled}" />
```
And there isn’t really much we can do here. Unless, that is, we’re ready to cede control and stop controlling components with this approach.

## The Boolean Checklist

Our finalized example with the article text alignment results in a clearer (and cleaner!) API and it prevents inappropriate sharing of code and concerns.

So, next time you’re adding a boolean to your API, ask yourself:
- Is this boolean used to indicate a mutually exclusive control
- Will I use this boolean as a control mechanism to decorate a component with additional information?
- Does this boolean enable additional actions or flows?

If any of those are a “yes”, it’s a time to review your API and find a way to decouple your code.



