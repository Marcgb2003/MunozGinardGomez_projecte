# MUMEZ GUITARS
#### Por Marc Gomez Barceló, Ruben Muñoz y Sergi Ginard
#### Nuestro proyecto consiste en una página web de venta de guitarras personalizadas, dado que eso posibilitará y justificará que usemos formularios y javascript. Está inspirada en la web de Sabrafen, un luthier español y tenemos planeadi implementar diversos modelos de guitarra.

## Diseño HTML de la web

Todas las páginas comparten el mismo header y footer para mantener coherencia visual y facilidad de navegación.

### Header general
El header tiene nuestro logo y redireciones a todas las páginas que tiene nuestra web para facilitar el movimiento entre estas. Consta de un img y 4 a que nos redireccionan
### Footer general
 El footer de nuestra página tiene links a nuestras redes sciales, nuestras vías de contacto y la dirección, junto con nuestro logo.

### Index
Es nuestra página principal, donde  tenemos un showcase de nuestras 4 guitarras principales, un extracto de nuestra presentación para que la gente nos conozca y una pequeña introducción de los servicios que ofreceremos, siendo esas 3 cosas artículos dentro de nuestro main.

### About Us
Nuestraa página contiene nuestra introducción como luthiers y el por qué lo hacemos y nuestra dirección, junto con un mapa embebido de google maps que te muestra exactamente donde está.

### Products
Esta página es tan solo un showcase de nuestros modelos de guitarra en el que, cuando implementemos el CSS, se verán en una tabla de tamaño variable dependiendo del tamaño de la pantalla.

### Product
En esta ágina veremos un showcase de las fotografías de nuestra guitarra y una breve descripción y luego una tabla de especificaciones de la susodicha guitarra.

### Services
Tenemos  un showcase de los servicios que ofrecemos junto con una imagen que muestra cada servicio que ofrecemos.

## Estado del Proyecto

Actualmente, esta web es un prototipo en desarrollo. La información y los textos presentes no están completos y pueden estar sujetos a cambios.

En el futuro, al pulsar sobre la foto de una guitarra, se redirigirá directamente a la página de producto correspondiente, funcionalidad que será implementada próximamente. Actualmente todas las fotografías que no son los modelos de guitarra son un placeholder genérico que se sustituira en cuanto tengamos el logo.

## Diseño CSS de la web

### Diseño visual

Hemos seguido un diseño sencillo, donde las fotografías sean lo principal y muy inspirado en la pagina web de Sabrafen, donde los diferentes blogs de información queden bien marcados y diferenciados. Queremos que la web sea accesible visualmente y que sea vendible, por lo que hemos usado Arial, sans-serif de tamaño 1rem y queremos que todo se diferencie bien. También hemos añadido que en la página de productos tengas un carrusel de imágenes y así puedas scrollear entre ellas.

### Responsiveness

Hemos diseñado esta web de manera que se autoajusten los layouts para que quepan en cualquier dispositivo, como se puede comprobar en nuestro navbar en cualquier página, nuestra página principal o, más visualmente, en nuestra página products, donde puedes ver que, según el tamaño, las guitarras se reordenan.

### Reparto de tareas

En esta parte nuestras tareas se han diferenciado, encargándose Ruben del responsiveness general y las decisiones visuales, Marc del mantenimiento y la cohesión del HTML con los cambios y el añadido de detalles para seguir con el diseño en todos los CSS y Sergi se ha encargado de crear el carrusel

## Diseño de formularios

### Diseño base

Hemos implementado una página de login a la cual se puede acceder desde cualquier otra página y que te pedirá el usuario y la contraseña y, cuando tengamos uso de Javascript y base de datos, te permitirá iniciar sesión.

A su vez hemos implementado una sección de mensaje directo en el about us donde le pedimos el nombre completo, la dirección de correo y el mensaje que desea enviar, lo cual será reenviado directamente a mi correo.

### Las verificaciones

En login tenemos los siguentes requisitos para el usuario: que acepte todas las letras tanto en mayúscula como en minúscula, todos los números, "-" y "\_" y que la contraseña tenga entre 4 y 30 caracteres, que incluya alguno de los siguientes caracteres: "\_-.:,;!"·$%&/()=?¿\|@#~" a parte de las letras tanto en mayúsculas como en minúsculas y los números.

En el mensaje hemos puesto que, como tiene que ser un nombre completo, tiene que incluir mínimo un espacio y que solo pueda tener letras tanto en mayúculas como en minúsculas y que el correo tenga una parte local que solo incluya letras, números y ".", un "@", la parte de dominio tenga los mismo requisitos que la parte local con el añadido de que puede contener un "-" y por último, separado por un ".", debe tener el tramo de dominio que solo pueden ser letras y debe tener como mínimo 2 caracteres.

### Reparto de tareas

Marc se ha encargado del HTML, mientras que Rúben ha puesto sus habilidades con el CSS y el diseño a buen uso y Sergi ha explicado el trabajo anteriormente mencionado en el README y ha ayudado en las decisiones de seguridad.

## Implementación de Javascript

### Modo claro/modo oscuro

Hemos implementado un botón en todos los headers que, al clickarse, invoca la función toggleTheme que revisa en el documento el valor de data-theme, si es dark da true, y si no da false. Luego usando ese booleano decide el nuevo tema, es decir, si el tema es dark, lo pone a light y viceversa. Después de eso aplica el nuevo tema, cambia el botón al botón del tema correspondiente y luego guarda el valor en localStorage para que al recargar la página se mantenga. Luego en el css hemos creado un check que si data-theme es dark, carga los valores de color del tema oscuro y si no lo deja con los colores básicos.

### Efectos del ratón


### Mostrar/Ocultar una tabla

Hemos creado la función toggleTable que coge la tabla que creamos y el botón que llama a su misma función y revisa el valor de collapsed de la tabla. Si la tabla está ya escondida lo añade al botón y a su vez pone un atributo llamado aria-expanded al botón para que los lectores de pantalla puedan saber si la tabla está escondida o no. Luego en el css, si el atributo collapsed de la tabla es true la vuelve invisible y si button tiene el atributo collapsed, lo gira 180 grados.

### Validación de datos

He creado una función que añade un eventListener al botón de submit, y que, cuando es pulsado, comprueba que los campos estén llenos y, si no para el envío de la información y saca un mensage de error.

### Creación del muro de comentarios

Hemos creado un artículo que hará de muro y zona de post de comentarios