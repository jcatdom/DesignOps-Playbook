# Figma UI Kits 

En Adevinta disponemos de UI Kits en Team Libraries de Figma para acelerar los procesos de diseño. Están estructurados con nuestro [sistema atómico](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/Atomic-design.md) y nos permiten tener una estructura reutilizable, escalable y que nos proporciona consistencia en nuestros productos. 

![](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/ASSETS/figma-1.png?raw=true)
> *UI Kits Adevinta*

## Estructura Adevinta

### UI Kits por vertical

Cada vertical cuenta con las librerías necesarias para trabajar sus proyectos y dispone de ellas de forma automática cuando se empieza un nuevo archivo.

![](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/ASSETS/figma-2.png?raw=true)
> *Ejemplo de librerías automáticas en Figma*
	
Puedes desactivar los UI Kits que no necesites para un proyecto y así hacer foco en los que sí vas a utilizar. Podrás reactivarlos más adelante si por ejemplo, el proyecto crece a otra plataforma y necesitas hacer uso de otro UI Kit.

![](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/ASSETS/figma-3.png?raw=true)
> *Activar/Desactivar librerías en Figma*

## Uso de componentes

### Instancias

Las instancias son copias de componentes reutilizables en diseño (las verás representadas en Layers con un rombo lila vacío). Están ligadas a un componente de origen (ya sea de una librería o  del propio documento) y recibirán todas las actualizaciones que se hagan sobre el componente.

![](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/ASSETS/figma-4.png?raw=true)
> *Ejemplo de componente e instancias*

Estas instancias permiten customizar el contenido en cada copia (icono, texto..).
Si necesitas cambiar espaciado de los elementos, su orden o añadir un nuevo elemento, deberás hacerlo desde el propio componente (más info debajo en Iteración de componente). 


### Variables

Algunos de los componentes cuentan con variables de customización. Cuando tengas seleccionada  una instancia de un componente, verás qué posibilidades permite en el sidebar de la derecha.

![](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/ASSETS/figma-5.png?raw=true)
> *Ejemplo de variables en componente*

Puede que los componentes además cuenten con componentes anidados. Haciendo doble click sobre un elemento, podrás ver si dispone de más opciones de customización con sus respectivas variables.

![](https://github.com/turolopezsanabria/design-systems-playbook/blob/chris/ASSETS/figma-6.png?raw=true)
> *Ejemplo de variables anidadas en componente*

ℹ️ Algunos componentes no tienen representadas todas sus variaciones (p.e: los Buttons en SUI Components no representan los estados desabilitados). Si necesitas mostrar un estado no diseñado en un ejemplo específico del diseño, puedes crearlo cambiando las propiedades de esa instancia del componente o si realmente crees que sería útil contemplar esas variables en la librería, consúltalo con tu UX Team si también le ven esa utilidad y puedes crearlas sin ningún problema. 


### Iteración de componente

Antes de iterar un componente de una librería primero debes comprobar si: 

1. El componente no te permite la customización que necesitas a través de sus variables.
2. La iteración que propones funcionará en los lugares donde ya se está utilizando el componente (habla con FE si no sabes donde se está utilizando).
3. La iteración es acorde al resto de tu UI Kit y al [Brand Manual] de tu vertical.
4. La iteración es factible para FE y aplica en ese componente y no en un componente anidado (habla con FE para que te explique como está montado. Quizás descubras que puedes hacer mucho más!).

Una vez comprobado, deberás iterar tu componente en el UIKit y actualizar la librería escribiendo un mensaje de commit (más info debajo en Control de versiones) para que otros UX puedan hacer uso. Paralelamente, deberás movilizar su creación en código dependiendo del proceso en el que estés trabajando tu proyecto (jira en tu team o issue de github). 


### Nuevo componente

Antes de crear un nuevo componente a una librería primero debes comprobar si: 

1. No hay otro componente existente que te pueda funcionar.
Podría ser una variable de un componente existente. 
2. El componente que estás creando tendrá un uso recurrente en tu vertical. En caso contrario no lo deberías componentizar (FE te ayudará a detectarlo).
3. El componente que estás creando es acorde al resto de tu UI Kit y al [Brand Manual] de tu vertical.
4. El componente es factible para FE y habéis acordado su creación.

Una vez comprobado, deberás crear tu componente en el UIKit y actualizar la librería escribiendo un mensaje de commit (más info debajo en Control de versiones) para que otros UX puedan hacer uso. Paralelamente, deberás movilizar su creación en código dependiendo del proceso en el que estés trabajando tu proyecto (jira en tu team o issue de github). 

### Control de versiones
Cuando vayas a subir una actualización de una librería, recuerda poner un mensaje de commit sobre qué estás actualizando. Es muy útil para el resto de UX que hagan uso de ella porque tendrán que aceptar estas actualizaciones en sus proyectos y deberán saber que es lo que ha cambiado. 
Además, nos permite tener un mayor control histórico de lo que estamos diseñando y nos da la posibilidad de volver a un paso anterior si hemos cometido errores.


### Nueva librería
Si necesitas crear una nueva librería para tu vertical, contacta con Design Ops para que la active y puedan utilizarla el resto de UX.
