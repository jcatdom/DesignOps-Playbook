# Colour

En Adevinta Spain tenemos múltiples paletas de colores, al menos una por cada marca, y cada una de ellas puede variar ligéramente de una aplicación a otra.

## Dos and Don'ts

{% hint style="success" %}
test de un success (do)
{% endhint %}

{% hint style="danger" %}
test de un danger (don't)
{% endhint %}

{% hint style="warning" %}
test de un warning
{% endhint %}

{% hint style="info" %}
test de un info
{% endhint %}

## Colores en SUI

Los componentes de SUI utilizan una paleta base que incluye los colores principales. Se encuentra en el [SUI Theme](https://github.com/SUI-Components/sui/tree/master/packages/sui-theme) y cada marca puede reemplazarla completamente.

![SUI Theme Palette](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-sui-theme-palette.png)

Por defecto, cada color tiene 4 tonos oscuros y 5 tonos claros, que se calculan automáticamente con una función de SCSS, que a su vez se puede personalizar en cada marca.

![Colours default Scale](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-shades-of-gray.png)

### ¿Debo usar las variaciones de color generadas automáticamente, o puedo usar colores propios?

Nuestra recomendación es sobreescribir cada color manualmente haciendo ajustes de accesibilidad. Si bien todos los componentes de SUI cumplen con una proporción de contraste adecuada, no podemos garantizar que el contraste sea correcto después de aplicar colores de marca.

Usa el plugin de Figma [Stark](https://www.figma.com/community/plugin/732603254453395948/Stark) y la web de colores accesibles [ABC](https://abc.useallfive.com) para ajustar tu paleta.

### ¿Estoy obligado a usar los 9 aunque mi marca no tenga tantos tonos?

No, si bien SUI Theme genera por defecto todos los tonos, esta escala puede ser sobrescrita, solo deberás "mapear" los tonos que no uses para cubrir todo el espectro.

Un pequeño detalle es que deberás ponerle un nuevo nombre a tus colores reducidos. En este ejemplo son `light` `lighter` `lightest`, pero podría ser `gray-1`, `gray-2`, `gray-3` o cualquier otra nomenclatura que hayáis acordado en vuestra marca.

![SUI Brand's theme map](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-shades-brand.png)

## Sistema de Tokens

### Tokens de color en el Theme de SUI

Al igual que con el resto de tokens, estos contienen un valor por defecto que se usará siempre y cuando no se provéa uno nuevo.

`$c-success: #00A544 default!;`

### Tokens de Componente en SUI Components

Los tokens de color de SUI Theme se usan en cada componente para definir diferentes propiedades.

En este ejemplo los dos componentes utilizan el mismo color `success` para sus `bgc` (background colour).

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-token-2.png)

### Tokens de color en el Theme de cada marca

Si una marca sobreescribe un token de color, todos los componentes que usen ese token heredarán la nueva definición.

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-token-3.png)

### Tokens de Componente en el Theme de cada marca

Yendo un paso más allá, cualquier Theme de marca puede sobreescribir los tokens de componente, como en este ejemplo donde `notification` y `badge` tienen ahora diferentes backgrounds.

![](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-token-4.png)

### ¿Existe un sistema de Tokens en Figma unificado para iOS Android y Web?

Si, pero solo en algunas de nuestras marcas. Esta es la lista completa:

* **Milanuncios**: Paletas diferentes, en una sola librería de Figma
* **Coches y Motos net**: Paleta única, en una sola librería de Figma
* **Cochesnet Pro**: Paleta única, en una sola librería de Figma
* **Fotocasa**: TBD
* **Fotocasa Pro**: TBD
* **InfoJobs**: TBD
* **ePreselec**: TBD

### RGB, HSL, HEX ¿Cuál debo usar?

DesignOps recomienda siempre usar HSL (tinta, saturación y luminosidad) porque ayuda a diseñadores y desarrolladores a tener una imagen más intuitiva de la construcción y ajuste de las paletas de color.

[Color scale](https://hihayk.github.io/scale/) es la herramienta recomendada si quieres hacer ajustes de color:

### ¿Dónde están los colores de mi marca?

Cada marca tiene un Theme propio que sobreescribe los colores por defecto de SUI. Algunas marcas tienen un repositorio específico, y otras han inlcuido el Theme en el monorepo de sus WebApps.

* [Milanuncios](https://github.mpi-internal.com/scmspain/frontend-ma--web-app/blob/master/theme/src/settings/\_color.scss)
* [Coches y Motos net](https://github.mpi-internal.com/scmspain/frontend-mt--web-app/blob/master/theme/src/shared/\_settings.scss)
* [Coches.net Pro](https://github.mpi-internal.com/scmspain/frontend-cf--web-app/tree/master/theme)
* [Fotocasa y Fotocasa Pro](https://github.mpi-internal.com/scmspain/frontend-fc--web-server/blob/master/theme/src/settings/\_colors.scss)
* [Inmofactory](https://github.mpi-internal.com/scmspain/frontend-if--uilib-theme/blob/master/src/settings/\_color.scss)
* [Habitaclia](https://github.mpi-internal.com/scmspain/frontend-hab--uilib-theme/blob/master/src/settings/\_color.scss)
* [InfoJobs](https://github.mpi-internal.com/scmspain/frontend-ij--uilib-theme/blob/master/src/tokens/\_color.scss)
* [ePreselec](https://github.mpi-internal.com/scmspain/frontend-ep--uilib-theme/blob/master/src/settings/\_colors.scss)

### ¿Tenemos Dark y Light Themes?

Por el momento no tenemos dark y light themes en nuestras aplicaciones web y componentes de Adevinta y SUI.
