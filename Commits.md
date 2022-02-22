# Commits

**Use `npm run co`**

Regardless if you work in Adevinta (you create branches) or you are collaborating from the outside (you fork the project) it is extremely important that you don't use `git commit` directly.

Use `npm run co` instead. This command triggers a wizard that writes a special commit message that is used later to decide if the contribution will be deployed as a `MAJOR` or `MINOR` version. In short, do the following:

{% code title="_settings.scss" %}
```js
$git add [your changes]
$npm run co
$git push
```
{% endcode %}