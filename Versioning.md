# Versioning

{% hint style="info" %}

### Each of our artifacts have its own Version Control System

The same component `button` can be `v1.2.0` in React and `v3.0.0` in Apps and, at the same time, not even have a version name in Figma.

{% endhint %}

#### How do we sync the versions of the same component in different platforms?

We don't force different platforms to converge in version name.

Once a component is designed and defined, each platform is responsible for using and delivering the latest experience to customers.

## Version control in SUI Components

Each component has its own version. There's no such thing as `@s-ui v2.1.0` but `@s-ui/react-atom-button 1.69.0` instead.

For each component we follow `MAJOR.MINOR.PATCH` standard, although we only use the first two.

* `MAJOR`: Breaking (incompatible) change.
* `MINOR`: Change that doesn't affect prior functionalities. Bug fixes without affecting backward compatibility.
* `PATCH`: Not used.


### How to commit work for SUI

{% hint style="info" %}
Use `npm run co`
{% endhint %}

Regardless if you work in Adevinta (you create branches) or you are collaborating from the outside (you fork the project) it is extremely recommended that you do NOT use `git commit` directly.

Use `npm run co` instead. This command triggers a wizard that writes a special commit message that is used later to decide if the contribution will be deployed as a `MAJOR` or `MINOR` version. In short, do the following:

```
$git add [your changes]
$npm run co
$git push
```

## Version control in Figma UI Kits

In contrast to code, all the Components in Figma live in a single file, we don't publish a single library per component and we don't name our UI Kits in Figma following MAJOR.MINOR.PATCH either.

You can use the libraries on the base that they are always up to date.

### Figma branches

Maybe this changes in the future but we have not found a valuable use for the feature _"branches"_ from Figma (yet).
