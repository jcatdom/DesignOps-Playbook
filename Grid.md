La Grid es la base para colocar elementos en pantalla. Diseñar según la Grid ayuda a crear experiencias fluidas, consistentes y fáciles de seguir.

Un uso constante de un sistema de cuadrícula proporciona la base para colocar elementos en pantalla de manera alineada. Facilita la comprensión y pone orden en la página.

## SUI Grid
To implement the grid, you need to use the two components it provides ```<LayoutGrid />``` a container, while each ```<LayoutGridItem />``` will as a cell to define your grid with the size you specify for each one of them. It only manages its inner space not adding unnecessary extra margins or paddings.

Further information and demo of [SUI Grid System](https://sui-components.vercel.app/workbench/layout/grid/demo).

## Anatomía
![Grid Anatomy](https://raw.githubusercontent.com/turolopezsanabria/design-systems-playbook/master/ASSETS/Grid-elements.png)

### Columnas
Las columnas son los bloques verticales imaginarios y se utilizan para alinear el contenido. Definimos los anchos de columna en porcentaje (%) o valores fijos.

El número de columnas que utilizamos es base 12. Un sistema de 12 columnas nos permite un mayor número de divisores, por lo que podremos conseguir una mayor combinación de posibilidades.

¿Y por qué no optar por un sistema de más columnas? Porque también buscamos la simplicidad. Podríamos tener un sistema más preciso, con mayor número de divisores, usando un sistema de más de 12 columnas, pero lo que ganamos en flexibilidad lo perderíamos en facilidad de uso.
Por ejemplo 1, 2, 3, 4, 6 o 12 son algunas de las estructuras de columnas que podemos utilizar. El número de columnas dependerán de los requisitos de diseño.

### Gutters
Los gutters son los espacios entre las columnas. Los gutters ayudan a separar el contenido. Definimos los anchos de gutter como valores fijos.

### Margins
Los márgenes son el espacio entre el contenido y los bordes de la pantalla. Definimos los anchos de los márgenes laterales como valores fijos que deciden el espacio mínimo que respirará cada tamaño de pantalla. Los márgenes flexibles ocupan el espacio restante que queda después de componer una Grid con columnas, gutters y márgenes laterales. Los márgenes flexibles cambian según los diferentes tamaños de pantalla.

## Grids en Adevinta

- [Real Estate](https://www.figma.com/file/WiMaTLdzoiiKFPITd3ymbC/?node-id=123%3A1620)
