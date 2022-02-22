# Version control in SUI Components

We don't publish a global SUI Version, there's nothing such as `@s-ui v2.1.0`

Each component has its own version: 

`@s-ui/react-atom-button 1.69.0`

For each component we follow `MAJOR.MINOR.PATCH` standard, although we only use the first two.

* `MAJOR`: Breaking (incompatible) change.
* `MINOR`: Change that doesn't affect prior functionalities. Bug fixes without affecting backward compatibility.
* `PATCH`: Not used.

{% hint style="info" %}

### Each of our artifacts have its own Version Control System

The same component `button` can be `v1.2.0` in React and `v3.0.0` in Apps and, at the same time, not even have a version name in Figma.

{% endhint %}

#### So... how do we sync the versions of the same component in different platforms?

We don't force different platforms to converge in version name. Once a component is designed and defined, each platform is responsible for using and delivering the latest experience to customers.