# Atomic design

Nuestras librerías de diseño se basan en un sistema atómico en el que contemplamos diferentes niveles en sus componetizació. Esto nos permite tener un sistema reutilizable, escalable y que nos proporciona consistencia en nuestros productos. 

![](https://www.solidbackgrounds.com/images/851x315/851x315-antique-white-solid-color-background.jpg)
> *Nuestra estructura atómica*

## Estructura

### Tokens
Son los estilos visuales aplicados a nuestros componentes (p.e: colores, tipografía, espacios..) definidos en nuestras plataformas como entidades con nombre que almacenan los atributos de diseño visual. Nos permiten mantener un sistema visual escalable y consistente. 
<br/> Más información sobre [Tokens](https://github.com/turolopezsanabria/design-systems-playbook/blob/master/Tokens.md).

### Átomos
Son los componentes indivisibles de nuestra librería (p.e: buttons, labels, inputs..). Pueden utilizarse de manera independiente en nuestras páginas aunque suelen estar ligados a moléculas y/u organismos. 
<br/>⚠️ Tienen unos tokens definidos y deberemos tener cuidado en su modificaciónn porque pueden estar ligados a varios componentes (p.e: el átomo Label se utiliza en las moléculas InputField, SelectField, TextareaField...) 

### Moléculas
Son combinaciones de átomos que funcionan juntos como una unidad (p.e: la molécula InputField está compuesta por los átomos Label, Input y HelpText). Nos permiten definir un propósito más elaborado de un componente (su comportamiento, interacción, estados..) y suelen contemplar variables para flexibilizar su uso (p.e: la molécula TextField permite no mostrar el átomo HelpText). 
<br/>Son la base de nuestro sistema de diseño y nos permiten agilizar la creación de nuestros productos.

### Organismos
Son componentes relativamente complejos compuestos de moléculas, y/o átomos y/u otros organismos. (p.e: nestedCheckboxes, Header..). Permiten formar diferentes secciones de una interfaz y definir interacciones claves de nuestros productos.

ℹ️ Si necesitas generar una nueva variable de cualquier componente, tendrás que verificar si lo que necesitas modificar es el organismo, las moléculas que lo componen o sus átomos. 
<br/>Más información sobre [cómo iterar un componente](https://github.com/turolopezsanabria/design-systems-playbook/blob/master/SUI-Components.md).

### Templates
Gracias a nuestro sistema átomico (átomos, moléculas y organismos) podemos generar templates de pantallas que definan nuestros productos de manera consistente.



## Organización en Adevinta

### Web 
Todas las plataformas utilizamos nuestra librería open-source de React SUI Components cuando refactorizamos nuestros productos. Sigue a la perfección este sistema atómico y te permite agilizar tanto tus diseños como la implementación.
Actualmente por diferencias entre plataformas, compartimos 100% los átomos y moléculas pero nos desvinculamos en organismos y templates donde cada plataforma cuenta con su espacio propio para ello. 
<br/>Iremos incorporando componentes donde veamos una posible reutilización global para agilizar aún más la creación de nuestros productos. 
<br/>Más información en [SUI-Components](http://localhost/). 

**Contamos con otros apartados comunes en web:**

+ **Behaviour:**
Unificamos comportamientos de interacción entre plataformas. Actualmente contamos con el behaviour Sticky, pero podemos unificar otros comportamientos a futuro como Reorder, Floating..

+ **Layout:** Contamos con una estructura definida y customizable de Grids. A futuro incorporaremos otros apartados comunes como Breakpoints, Spacing, Responsive..


### Native (iOS & Android) 
Utilizamos un sistema similar pero desvinculado de SUI (algunas plataformas si lo utilizan). Tenemos definidos unos tokens unificados con Web dentro de sus posiblidades, componentes específicos de cada plataforma native (que formarían estos átomos y moléculas. P.e: app bars, buttons, chips…) y componentes específicos de la plataforma (que serían los organísmos. P.e: cardX, cardY…) Aún así no generamos esta escala atomizada de 3 niveles.

### Design vs Code
UX cuenta con las librerías de diseño necesarias para su plataforma en Figma unificadas al código de nuestros productos. Esto nos permite la agilización y escala de nuevas implementaciones. 
<br/>Tienes más información en [Figma-UI-Kits](https://github.com/turolopezsanabria/design-systems-playbook#:~:text=16%20days%20ago-,Figma%2DUI%2DKits.md,-init) y respecto a las librerías de código en [ SUI-Components??](https://github.com/turolopezsanabria/design-systems-playbook/blob/master/SUI-Components.md)


