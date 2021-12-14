# Color

En Adevinta Spain tenemos múltiples paletas de colores, al menos una por cada marca, y cada una de ellas puede variar ligéramente de una aplicación a otra.


### ¿Existe un sistema de Tokens en código unificado para iOS Android y Web?

No,todavía no tenemos unificado un sistema de Tokens universal que garantice el uso de cada color en todas las plataformas.

En este artículo encontrarás tanto los aspectos generales de las 3 plataformas como también las particularidades de cada marca y apliación en datalle.

### ¿Existe un sistema de Tokens en Figma unificado para iOS Android y Web?

Si, pero solo en algunas de nuestras marcas. Esta es la lista completa:

- Milanuncios: Paletas diferentes, en una sola librería de Figma
- Coches y motos net: Paleta única, en una sola librería de Figma
- Cochesnet Pro: Paleta única, en una sola librería de Figma
- Fotocasa: TBD
- Fotocasa Pro: TBD
- InfoJobs: TBD
- ePreselec: TBD

### RGB, HSL, HEX ¿Cuál debo usar?

DesignOps recomienda siempre usar HSL (tinta, saturación y luminosidad) porque ayuda a diseñadores y desarrolladores a tener una imagen más intuitiva de la construcción y ajuste de las paletas de color.

Esta es la herramienta recomendada si quieres hacer ajustes de color:

[Color scale](https://hihayk.github.io/scale/)


## Colores en SUI 

### ¿Dónde están los colores de SUI Components?

La paleta de colores se encuentra en el SUI Theme, puedes visitarlo en [este repo](https://github.com/SUI-Components/sui/tree/master/packages/sui-theme).

Los componentes de SUI utilizan esta paleta como base, y cada marca puede reemplazar los colores con la suya propia.

### ¿Existen Dark y Light Themes en SUI Components?

No, no hay temas de dark mode en web para los componentes de SUI, los componentes de Adevinta.

### ¿Cuántas paletas de colores hay en SUI?

Solo una, SUI Theme no incluye colores de marca, solo tiene una paleta principal que incluye Black, White, Primary, Accent, Gray, Success, Alert y Error

<img src="https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-sui-theme-palette.png" alt="SUI Theme palette"/>

### ¿Cuántas variaciones de tonos claros y oscuros hay para cada color?

Por defecto, para cada uno de los colores hay 4 variaciones de tonos oscuros y 5 variaciones de tonos claros.

<img src="https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-shades-of-gray.png" alt="SUI Theme shades"/>

### ¿Cómo se calculan las variaciones de tonos claros y oscuros en el Theme de SUI?

El gradiente de color es calculado automáticamente por esta función de SCSS, que a su vez puede ser personalizada en cada marca.

### ¿Dónde están los colores de mi marca?

Cada marca tiene un Theme propio que sobreescribe los colores por defecto de SUI. Algunas marcas tienen un repositorio específico, y otras han inlcuido el Theme en el monorepo de sus WebApps.

- [Milanuncios](https://github.mpi-internal.com/scmspain/frontend-ma--web-app/blob/master/theme/src/settings/_color.scss)
- [Coches y Motos net](https://github.mpi-internal.com/scmspain/frontend-mt--web-app/blob/master/theme/src/shared/_settings.scss)
- [Coches.net Pro](https://github.mpi-internal.com/scmspain/frontend-cf--web-app/tree/master/theme)
- [Fotocasa y Fotocasa Pro](https://github.mpi-internal.com/scmspain/frontend-fc--web-server/blob/master/theme/src/settings/_colors.scss)
- [Inmofactory](https://github.mpi-internal.com/scmspain/frontend-if--uilib-theme/blob/master/src/settings/_color.scss)
- [Habitaclia](https://github.mpi-internal.com/scmspain/frontend-hab--uilib-theme/blob/master/src/settings/_color.scss)
- [InfoJobs](https://github.mpi-internal.com/scmspain/frontend-ij--uilib-theme/blob/master/src/tokens/_color.scss)
- [ePreselec](https://github.mpi-internal.com/scmspain/frontend-ep--uilib-theme/blob/master/src/settings/_colors.scss)


### ¿Debo usar la paleta generada por SUI Theme, o puedo generar una propia?

Nuestra recomendación es sobreescribir cada color manualmente haciendo ajustes de accesibilidad ya que, aunque todos los componentes de SUI cumplen con una proporción de contraste adecuada, SUI no garantiza que el contraste sea correcto después de aplicar colores de marca.

Estas son las 2 herramientas recomendadas:

- [Stark plugin para Figma](https://www.figma.com/community/plugin/732603254453395948/Stark)
- [Accessible Brand Colors](https://abc.useallfive.com/)

### ¿Debo usar los 9 tonos aunque mi marca no tenga tantos?

No, si bien por defecto SUI Theme genera 9 tonos de cada color, esta escala puede ser sobrescrita. Si tu marca tiene menos tonos deberás "mapear" los tonos para cubrir todo el espectro.

<img src="https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/colour-shades-brand.png" alt="SUI Theme shades"/>


### Sistema de Tokens ¿Cuál es la jerarquía de color en SUI?

1. Tokens fundamentales (SUI Theme)
2. Tokens semánticos (SUI Theme y SUI Components)
3. Tokens de componente (SUI Components)
4. Tokens de marca que sobreescriben a los primeros tres
