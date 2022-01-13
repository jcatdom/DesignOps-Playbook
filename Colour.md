# Colour

Each brand should have its own colours. Your brand can have as many colours and colour variations as you wish.

## Colour implementation

Each technology and platform has it own rules and subtle implementation variations but, in general, your brand colours should rule over platform specifics.

### Colours in SUI

The components in SUI use a base palette of colours. It's located in [SUI Theme](https://github.com/SUI-Components/sui/tree/master/packages/sui-theme), a base theme each brand can override completely.

![SUI Theme Palette](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-sui-theme-palette.png)

SUI Theme provides 4 shades of darkness and 5 shades of lighness by default. These colours are generated automatically using a SCSS function you can override as well.

![Colours default Scale](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-shades-of-gray.png)

### You are not obliged to use the shades generated automatically 

We recommend you override each of the shadesmanualy with special focus on accessibility. Although we initially ensure each component complies with contrast A11y standards, we can't ensure they will work after replacing ours with your brand colours.

Use this plugin for Figma [Stark](https://www.figma.com/community/plugin/732603254453395948/Stark) and the contrast website  [ABC](https://abc.useallfive.com) to refine your palette.

### You are not obliged to use all the 9 shades SUI generates

Although SUI will always generate 9 shades for each colour, you can map them to match your number of colours.

A small detail: The name of your colour scale needs to be different from SUI's. In our example the new `Gray` is called `Bluestone` and it's variations are `light` `lighter` `lightest` `dark` `darker`

![Bluestone is Gray](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-gray-brand.png)

Once you map the new colours the range of grays gets smaller while preserving 9 steps.

![SUI Brand's theme map](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-shades-brand.png)

## Tokens system

### Colour tokens in SUI Theme

Same as with the rest of tokens, each colour in SUI has a default value that will be used unless it's overriden at any point.

`$c-success: #00A544 default!;`

### Component Tokens

All the colours in SUI Theme are used to define styles in components tokens:

In this example both components use the same colour `success` for `bgc` (background colour).

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-token-2.png)

### Overriding Tokens on a Brand Theme

If you override a colour token in your theme, every component using that token will change.

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-token-3.png)

### Overriding Component Tokens on a Brand Theme

If you override a component token in your theme, just the element using that component token will change.

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-token-4.png)

### Brand themes

Each brand has a specific repo, some of them as independent repo and some as part of a bigger app (mono-repo)

* [Milanuncios](https://github.mpi-internal.com/scmspain/frontend-ma--web-app/blob/master/theme/src/settings/\_color.scss)
* [Coches y Motos net](https://github.mpi-internal.com/scmspain/frontend-mt--web-app/blob/master/theme/src/shared/\_settings.scss)
* [Coches.net Pro](https://github.mpi-internal.com/scmspain/frontend-cf--web-app/tree/master/theme)
* [Fotocasa y Fotocasa Pro](https://github.mpi-internal.com/scmspain/frontend-fc--web-server/blob/master/theme/src/settings/\_colors.scss)
* [Inmofactory](https://github.mpi-internal.com/scmspain/frontend-if--uilib-theme/blob/master/src/settings/\_color.scss)
* [Habitaclia](https://github.mpi-internal.com/scmspain/frontend-hab--uilib-theme/blob/master/src/settings/\_color.scss)
* [InfoJobs](https://github.mpi-internal.com/scmspain/frontend-ij--uilib-theme/blob/master/src/tokens/\_color.scss)
* [ePreselec](https://github.mpi-internal.com/scmspain/frontend-ep--uilib-theme/blob/master/src/settings/\_colors.scss)

### We don't have a unified token system for Web and Apps

Some brands have started efforts to normalise colours in a single format, check their UI Kits

### RGB, HSL, HEX?

We recommend you always start with HSL (hue, saturation y lightness). It's the most intuitive way to create correct palettes for designers and developers.

Use this great tool: [Color scale](https://hihayk.github.io/scale/)

### Dark Themes

**We don't have dark-mode in any of our Web Applications**

CarFactory/Coches.net Pro has been dark-mode by default for a long time but has recently grown into light-mode.

**What about native Apps**

Although all brands have worked on it, only infoJobs has implemented dark mode in production for their iOS App.

Jobs have also implemented some screens in darkMode in Android but, in order to deliver a consistent experience, these pages won't be enabled until the whole App has been refactored.
