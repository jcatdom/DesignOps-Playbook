# Mobile 1st

Mobile first, significa que comenzamos el diseño de producto desde el extremo Mobile que cuenta con más restricciones y posteriormente expandimos las funciones para crear una versión Tablet y Desktop.

Para ello, tendremos en cuenta los siguientes puntos:

## Responsive web design

  Todos nuestros productos web son responsive (diseño adaptable). Esto permite que se ajuste el contenido automáticamente a las pantallas de los diferentes dispositivos y lo muestra de manera que las personas se sientan cómodas sin tener que desplazarse lateralmente, hacer zoom…


## Progressive advancement

  Primero diseñamos una versión para el navegador relativamente más bajo con las funciones y características básicas. Posteriormente crearemos las versiones para Tablet y Desktop agregando las modificaciones oportunas: mostrar más campos, utilizar una grid más compleja, interacciones o efectos más complejos y aprovechando el estado Hover… de esta manera, conseguiremos crear una experiencia acorde a cada dispositivo útil para las personas. 

  ⚠️ Por el contrario, el uso de “Grateful Degradation” qué propone iniciar el diseño de producto desde un extremo avanzado Desktop e ir cortando funcionalidades o contenidos para versiones Mobile, harán que inevitablemente se quiera aprovechar todas las opciones y generar una experiencia no acorde al dispositivo para las personas. Por lo que no debemos realizar este procedimiento de diseño en nuestra compañía.
  

**Tomando como punto de partida la versión Mobile, aprovecharemos los puntos clave de un producto para fortalecerlo en su versión Desktop.**


## Componentes de SUI

De cara a nuestros componentes, contamos con mismos acuerdos mobile first:

Every component in SUI should follow a Mobile 1st approach.

In practical terms it means not only that each component should work perfectly in a mobile device, but also that every new Design, Discussion, Suggestion or Pull Request should take that into consideration.

### Follow these simple rules:

- The design specs must be for mobile first
- Avoid displaying more information on hover (such as tooltips)
- Provide solutions for touch only devices that don't provide hover
- Think how the elements will behave if they are forced to break in more than on line
- etc
