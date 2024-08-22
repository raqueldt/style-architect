# Instrucciones para el Desarrollo Utilizando SASS

## Objetivo
Desarrollar una estructura de estilo utilizando SASS que incorpore prácticas de codificación como el uso de variables, modularidad, mixins y el correcto uso de las etiquetas HTML.

## Requisitos
- Conocimientos básicos de HTML y CSS.
- Instalación de SASS en el entorno de desarrollo.
- Editor de texto o IDE que soporte SASS.

## Estructura de Archivos
Organiza los archivos SASS de la siguiente manera para facilitar el mantenimiento y la escalabilidad del proyecto:

### styles/
- **base/**: Estilos base como reset o normalize.
- **components/**: Estilos específicos de componentes.
- **helpers/**: Mixins y funciones reutilizables.
- **layout/**: Estilos para la disposición general de la página (header, footer, grid).
- **themes/**: Variables para temas de colores, tipografía, etc.
- **main.scss**: Archivo principal que importa todos los módulos.

## Uso de Variables
Define las variables en el archivo `themes/_variables.scss` para gestionar colores, tipografía, espacios, etc.

```scss
// themes/_variables.scss
$primary-color: #3498db;
$secondary-color: #2ecc71;
$font-primary: 'Helvetica Neue', sans-serif;
```

## Modularidad
Crea archivos separados para cada componente o sección de la página, asegurándote de que cada uno solo contenga los estilos específicos que necesita. Importa todos estos archivos en tu archivo `main.scss` para compilarlos en un solo CSS.

## Mixins
Utiliza mixins para estilos reutilizables, como botones, sombras, o transiciones. Define los mixins en `helpers/_mixins.scss`.

```scss
// helpers/_mixins.scss
@mixin button-style($bg-color, $text-color) {
  background-color: $bg-color;
  color: $text-color;
  padding: 10px 15px;
  border-radius: 5px;
  &:hover {
    background-color: darken($bg-color, 10%);
  }
}
```

## Uso Correcto de Etiquetas HTML
Asegúrate de que las etiquetas HTML usadas en el proyecto sean semánticamente correctas para los estilos que se aplican. Por ejemplo, utiliza `<header>`, `<footer>`, `<nav>` para las estructuras correspondientes y asegúrate de que los estilos SASS coincidan con estas estructuras.

## Estructura asignada
Se enfoca a la estructura general o macro de la pantalla, es decir lo que va a predominar en el diseño, también pueden incluir otras estructuras, pero la asignada es la que debe predominar.
## Evaluación
- **Claridad y organización del código**: El código debe ser fácil de entender (nombres, organizaición).
- **Eficiencia de los mixins**: Los mixins deben proporcionar ventajas claras como reusabilidad y reducción de redundancias.
- **Consistencia de los estilos**: Los estilos deben ser consistentes en todas las páginas y componentes.
- **Responsividad**: El diseño debe ser responsive y adaptarse a diferentes tamaños de pantalla.

## Presentación
- Muestra la implementación parcial en la próxima clase.
- Prepara una breve explicación sobre la estructura de tus archivos, el uso de variables y mixins, y cómo contribuyen a un mantenimiento eficiente del proyecto.
