# Versioning

**Each of our artifacts have its own Version Control system**

Native components don't share the same approach from Figma, or React Components.

i.e. The same component `button` from Figma can be `v1.2.0` in React and `v3.0.0` in Apps while not having a version name in design tools. 

> **How do we Sync the versions from different platforms?**

> We don't force different platforms to converge. Once UX is defined each platform is responsible for using and delivering the latest experience to customers.


## Version control in SUI Components

We follow MAJOR.MINOR.PATCH increment standards:

- MAJOR version is required everytime you make a breaking (incompatible) change.
- MINOR version if you make a change that doesn't affect prior functionalities.
- PATCH version to fix an existing bug without afecting backward compatibility.

Note: In practice we only work with "Major" and Minor versions.

### npm run co

Regardless if you wormk in Adevinta (you create branches) or you are collaborating from the outside (you fork the project) it is extremly recommended that you **do not** use `git commit` directly.

Use `npm run co` to commit your changes. This command is a wizard that asks questions and writes a special commit message that is used later to decide if the contribution will be deployed as a MAJOR or MINOR version.

In short:

- git add
- npm run co
- git push

## Version control in Figma UI Kits

In contrast to code, all the Components in Figma live in a single file, we don't publish a single library per component.

On top of that, we don't name our UI Kits in Figma following MAJOR.MINOR.PATCH standard.

You can use the libraries on the base that they are always up to date. Maybe this changes in the future but we have not found a valuable use for the feature _"branches"_ from Figma (yet).

