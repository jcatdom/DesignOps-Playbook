# Flexibility

The balance between flexibility and standardisation of our systems is a recurrent topic in our community, hence we revisit our agreements 2 times a year, and 3 things are clear every time we discuss it:

- Design Systems have benefits on speed, quality and consistency
- Design Systems **DO** limit your creativity within the system
- Design Systems **DON'T** limit your creativity outside of the system

## What if you can't find what you need in the System?

The 1st advice is to double-check, all our components provide a wide range of options for size, colours and variations.

In case the solution you need is not provided by the Design System:

- Iterate an existing component and include the variation you need
- Create a new component
- Create something new outside the system (Assess if it's worthy to make something from scratch rathet than stick to a similar solution already designed and coded)

## Types of "more flexibility" needs

Simplifying a lot, there are a few types of requests: Change how it works, change how it looks like, add a new variation.

### Changes on how it works

Sometimes you need an existing component with a little twist, for instance a new Shape.

In this case you can either add the new variation as a new Prop of the component (something like `shape {square, rounded, circle}`), or create a new component if you think the result will be too different to be considered the same component.

If the requested iteration is not widely needed (something really custom to a brand) it should not be included in SUI but as a Snowflake or a Drop of Water.

In case of doubt [open a discussion](https://github.com/SUI-Components/sui-components/discussions/categories/ideas-and-new-features)

### Changes on how it looks like

{% hint style="success" %}
You can change every style of a component in your theme
{% endhint %}

Almost everything in terms of colours, typography and spacing can be customised in your theme, as long as the change applies for all the instances of the component (If your primary color is blue, every component using a primary colour will be blue).

If the CSS property you want to adjust is not _customisable_ you can create a pull request to _open_ it. Here's an [example](https://github.com/SUI-Components/sui-components/pull/1952/files) to allow overriding the text decoration of links.

{% hint style="danger" %}
Don't use classNames to style components on the fly
{% endhint %}

We extremely recommend you don't style a component using it's class name. If you need to position a component in your layout wrap it inside a `<div>` and adjust that div instead. If you want to change something else such as a color, do it in your theme instead. It's the best way to ensure the integrity of your app in case we change something in the Design System that may cause your styles to break.