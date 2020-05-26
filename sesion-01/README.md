# Sesión: Estructura tu sitio

Sigue el contenido a continuación durante clase para que no te pierdas ningún
detalle de lo que estás a punto de aprender.

## Objetivos

En esta sesión aprenderás:

- Interactuar con la terminal para crear una estructura de archivos para tu
  proyecto.
- Crear una estructura base de tu página web a partir del uso de etiquetas de
  HTML.
- Personalizar la apariencia de tu página a través de cambios que se aplican a
  través de CSS.
- Usar comandos de GIT para almacenar tus cambios realizados en la red social
  más usada por lxs programadorxs (Github).
- Desplegar tu página para que sea visible a todo el mundo de una manera
  sencilla y gratuita.

## Contenido

### Creando la estructura de tu proyecto

Todo desarrollo de proyecto web se hace a través de código, comandos que
escribimos y que luego programas usan para traducirlo en algo que entienda la
computadora. Sin embargo, es necesario entender que la computadora solo entiende
1s y 0s, lo cual es muy complejo para nosotros como humanos entender. Debido a
esto, se crearon lenguajes que actúan como intermediarios entre las computadoras
y humanos. En esta sesión vamos a estar interactuando principalmente con 2
lenguajes: **HTML y CSS**.

Debido a que son 2 lenguajes con propósitos distintos, es importante mantener un
orden en los recursos que usaremos para construir nuestro sitio web, por lo cual
es importante que usemos una estructura ordenada para tener un mejor control y
entendimiento sobre como llevar a cabo nuestro proyecto. Dicha estructura la
construiremos usando comandos en nuestra terminal que indicarán a la computadora
que realice exactamente lo que nosotros le pidamos.

#### Concepto: Terminal

La terminal es un programa de computadora que nos sirve para indicar acciones
específicas que deseamos realizar. Todo lo que normalmente estamos acostumbrados
a realizar a través de la interfaz gráfica que nos aparece en nuestras pantallas
del computador y que con ayuda del _mouse_ y el _teclado_ podemos indicar lo que
queremos hacer es posible realizarlo a través de **comandos** escritos en la
terminal.

Por ejemplo, normalmente para crear un directorio (carpeta), entrarías a un
_Explorador de archivos_, y luego darías click hasta llegar a la ubicación donde
se desea crear, presionas click derecho y le das nueva carpeta o dependiendo de
la computadora que utilices encontrarás un ícono que te dará un acceso rápido a
realizar exactamente esta misma acción.

Si bien este flujo es normal y probablemente no lo dejemos de hacer por la
rapidez, velocidad, costumbre, entre otros factores. Como programadorxs,
acostumbramos a realizar las mismas acciones desde la terminal usando solo el
teclado, esto por la rapidez y control que se siente sobre la computadora, pero
también porque en algunas actividades que realizamos (sobre todo cuando
configuramos servidores) no contamos con una interfaz gráfica y la terminal se
vuelve nuestra única amiga.

> TIP: La terminal también es comúnmente llamada como _consola_, _CLI_, _bash_
> (no necesariamente bien usado), _shell_ (a pesar que no es lo mismo) y tal vez
> te encontrarás con otro término dependiendo de la persona de quien lo escuches
> o leas.

#### Guía: Creación de estructura de proyecto

1. Abrir la terminal (tener en cuenta que la interfaz puede cambiar dependiendo
   del sistema operativo que tengas).

2. Por defecto, cuando abrimos la terminal este se ubica en el directorio
   principal (_home_) de nuestro computador. Podemos verificar cuál es dicho
   directorio a través del comando `pwd`.

   ```bash
   $ pwd # Present Working Directory
   /Users/bedu
   ```

3. Una vez que sepas en donde te encuentras probablemente quieras ir a alguna
   otra ubicación para crear la carpeta del proyecto. Digamos que queremos
   crearlo dentro de la carpeta _Documents_ (el nombre puede variar dependiendo
   del sistema operativo). El comanto que nos permite acceder o movernos de
   ubicación es `cd`. A diferencia del comando anterior, éste es procedido por
   el nombre del directorio al que nos queremos mover.

   ```bash
   $ cd Documents # "Change Directory" a Documents
   ```

   > TIP: Si quieres verificar que realmente se haya cambiado de ubicación,
   > puedes usar el comando anterior para comprobarlo:
   >
   > ```bash
   > $ pwd
   > /Users/bedu/Documents
   > ```

4. Ahora que ya te encuentras donde deseas crear tu proyecto, es momento de
   crear un directorio donde almacenarás todos los archivos que terminarás
   utilizando. Para crear dicho directorio puedes usar el comando `mkdir`, al
   igual que `cd`, este comando necesita que le indiques el nombre del
   directorio que deseas crear.

   ```bash
   $ mkdir matcha # Make Directory "matcha"
   ```

5. El comando que acabas de ejecutar, ha creado una carpeta llamada `matcha`,
   una forma de verificar si se ha creado es listando todo lo que se encuentra
   en la ubicación actual. Para esto, usa el comando `ls`.

   ```bash
   $ ls # List
   matcha   another-directory    some-file.txt
   ```

   > TIP: Dependiendo de la configuración de tu terminal, puede que te muestre
   > las carpetas con un formato diferente al de los archivos, en caso contrario,
   > lo puedes diferenciar debido a que la mayoría de archivos contienen un
   > punto (`.`) seguido de la extensión (nombre particular, ejemplo: txt, doc,
   > xls, etc) mientras que los directorios no.

6. Una vez comprobado que tu directorio se creó correctamente, accede a él
   (recuerda el comando `cd` para cambiar de ubicación y `pwd` para verificar).
   Una vez dentro, el comando para crear archivos es `touch` seguido del nombre
   del archivo que deseas usar. Para este caso, crearemos solo uno llamado
   `index.html` (en este caso _.html_ es la extensión que usaremos).

   ```bash
   $ cd matcha # Change directory a "matcha"
   $ pwd # Present Working Directory
   /Users/bedu/Documents/matcha
   $ touch index.html # Crea archivo "index.html"
   $ ls # Lista contenido
   index.html
   ```

¡Genial! Acabas de crear la estructura mínima de tu proyecto usando la terminal
de tu computadora, ahora tienes el poder sobre ella y poco a poco te irás
olvidando de tu _mouse_ o _touchpad_. Lo que acabas de crear debe tener una
estructura similar a:

```text
Documents/
└── matcha/
    └── index.html
```

### Estructura tu página web

#### Concepto: HTML

Para definir el contenido de nuestra página web, es necesario hacer uso de `HTML`
(HyperText Markup Language). Este lenguaje de marcado nos permite expresar al
navegador web (programa que usamos para navegar en internet, ejemplo: Internet
Explorer, Google Chrome, Mozilla Firefox, Safari, etc) lo que queremos que se
muestre a través de una sintaxis basada en _etiquetas_.

La estructura de una etiqueta es como sigue:

```html
<!-- Esta línea es un comentario de HTML -->

<!-- Ejemplo de la sintaxis para agregar una imagen a nuestra página -->
<img src="https://bedu.org/logo.png" alt="Logo de Bedu" />

<!-- Ejemplo de la sintaxis para agregar un párrafo a nuestra página -->
<p class="paragraph">Este es un párrafo</p>
```

En el código anterior podemos ver la sintaxis de una imagen y un párrafo en HTML.
Si los analizamos podemos ver lo siguiente:

- Las etiquetas empiezan con `<` seguido del nombre de la etiqueta (`img`, `p`).
- Separados por espacios encontramos atributos. Estos siguen la sintaxis
  `nombre-atributo="valor-atributo"`.
- Los atributos pueden variar dependiendo del tipo de etiqueta (las imágenes
  usan `src` y `alt` pero los párrafos no).
- Para denotar el fin de la etiqueta `img`, usamos `/>`.
- Mientras que para etiquetas como la de párrafo (`p`), la etiqueta de apertura
  termina con `>`, seguido del contenido de lo que representa la etiqueta, y por
  último la etiqueta de cierre con la sintaxis (`</nombre-etiqueta>`).

> TIP: Al inicio puede verse complicado identificar que etiquetas se cierran
> automáticamente (como `<img />`) y cuáles necesitan cerrarse manualmente como
> la etiqueta `<p></p>`. La clave para comprender esto es que existen etiquetas
> que pueden tener contenido dentro de ellas (como texto o incluso más etiquetas)
> mientras que otras etiquetas no pueden contener nada dentro de ellas (como
> las imágenes).

Por último pero no menos importantes, los comentarios son bloques de texto que
no se muestran en la página web pero que sirve de información importante para
lxs programadorxs que leen/escriben el código. La sintaxis es `<!--`, seguido
del texto que queremos comentar y cerrando el comentario con `-->`. Tener en
cuenta que un comentario no se cierra hasta no encontrar la etiqueta de cierre.

Esto no mostraría nada en la web:

```html
<!-- Este es un comentario mal cerrado y que no permitirá mostrar el párrafo

<p>
Este párrafo está bien escrito pero no se mostrará por el comentario mal cerrado
</p>
```

#### Guía: Creando nuestro HTML

Es momento de abrir nuestro editor de texto (ejemplo: Visual Studio Code) y
abrir el directorio que creamos en dicho editor, selecciona tu archivo
`index.html` y prepárate para ensuciarte las manos.

Las etiquetas mínimas a incluir en todos los documentos de HTML que creemos son:

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Aquí va información importante pero no visible dentro del navegador -->
    <title>Matcha</title>
  </head>
  <body>
    <!-- Esto es lo que se verá en el navegador web -->
  </body>
</html>
```

Analicemos las etiquetas del código anterior:

- `<!DOCTYPE html>`. Esta etiqueta rompe con el patrón de las sintaxis vistas
  anteriormente, pero no te preocupes, es una de las únicas que tienen una
  sintaxis particular y la usarás para indicarle al navegador web la versión
  de HTML que usarás. En este caso, esta sintaxis está indicando que usaremos
  `HTML 5`. Resulta que `HTML` ha pasado por diversas versiones, la diferencia
  entre ellas son principalmente las capacidades que estas soportan, por ejemplo,
  más adelante te darás cuenta que existen etiquetas que te ayudarán a expresar
  mejor el tipo de contenido que estas reflejarán al navegador (ejemplo: `nav`,
  `section`, `header`, `footer`, entre otras) que en versiones anteriores del
  lenguaje no existían.

  Ejemplo de cómo indicar al navegador que usaremos HTML 4:

  ```html
  <!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">
  ```

  ¿Mejor nos quedamos con `HTML 5` no?

- `<html></html>`. Es momento de que te enteres que todo en HTML es una
  estructura jerárquica, y como en toda jerarquía siempre existe un extremo a
  partir del cual todo inicia. Esta es la etiqueta que indica el punto de partida
  de la página, todo lo que se encuentre dentro será el contenido que el
  navegador tomará en cuenta para mostrar a lxs usuarixs. Esta etiqueta en
  particular tiene 2 _"hijos"_ que encontrarás en todas las páginas web:
  `<head></head>` y `<body></body>`.

- `<head></head>`. En esta etiqueta se encontrará toda la información relevante
  del sitio web pero que no se muestran como tal. Por ejemplo, acá podemos
  indicar el título de la página, el ícono, si debe de importar algún estilo que
  personalice la apariencia de nuestro contenido, información de la descripción
  de la página para que se muestren en los resultados de búsqueda de internet,
  etc.

- `<title></title>`. Esta etiqueta permite indicar cuál es el título que el
  navegador debe mostrar cuando un usuario este navegando en nuestro sitio web.

- `<body></body>`. Esta etiqueta nos sirve para delimitar todo el contenido de
  la página web y es dentro de esta que encontramos todo lo que vemos cada vez
  que visitamos un sitio. Botones, textos, imágenes y demás se definen dentro
  de esta etiqueta.

#### Guía: Agregando el home de Matcha

Siguiendo el diseño del sitio original de [`Matcha`](https://getmatcha.com),
podemos ver que lo primero que nos muestra son textos de diferentes tamaños y
colores además de un formulario y una imagen.

Para agregar el texto principal podríamos usar un párrafo (etiqueta `<p></p>`),
sin embargo, este texto quiere reflejar lo que nos permite realizar el servicio
de `Matcha` y por ende dar un mayor énfasis y diferenciarlo de los demás textos.

Para lograr este efecto _semántico_ en nuestro sitio web, podemos usar los
_headings_ (encabezados). Estos nos ayudan a dar un énfasis jerárquico de
acuerdo al número que nosotros utilicemos, siendo posible usar del 1 al 6,
con 1 como el de mayor peso jerárquico y 6 lo contrario.

En este caso, queremos el texto inicial es el de mayor peso jerárquico por lo
que usaremos el heading de peso 1, y esto lo indicamos haciendo uso de la
etiqueta `<h1></h1>`.

Aplicándolo a nuestro código existente:

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Aquí va información importante pero no visible dentro del navegador -->
    <title>Matcha</title>
  </head>
  <body>
    <!-- Esto es lo que se verá en el navegador web -->
    <h1>Build your blog. Build your business.</h1>
  </body>
</html>
```

Abre este archivo en tu navegador y mira el resultado. ¡Tu primera página web!
Claro, solo es un texto, pero es un gran primer paso!

##### Challenge: Segundo texto

Así que, ¿por qué no le agregamos el siguiente texto que encontramos en la web
de `Matcha`? ¿Qué peso jerárquico y por ende qué etiqueta le pondrías al
encabezado? ¿Y si fuese un párrafo en vez de un encabezado? ¿Cuál sería la
diferencia?

##### Posible solución

```html
<!DOCTYPE html>
<html>
  <head>
    <!-- Aquí va información importante pero no visible dentro del navegador -->
    <title>Matcha</title>
  </head>
  <body>
    <!-- Esto es lo que se verá en el navegador web -->
    <h1>Build your blog. Build your business.</h1>
    <h4>
      Instantly publish articles, drive more traffic, grow your email list, and
      see your blog’s impact on sales.
    </h4>
    <!-- O usando un párrafo -->
    <!--
      <p>
        Instantly publish articles, drive more traffic, grow your email list,
        and see your blog’s impact on sales.
      </p>
    -->
  </body>
</html>
```

La principal diferencia es el peso semántico que le queremos dar al texto, si
el texto que queremos mostrar no es necesariamente diferente a cualquier otro
texto que tengamos en la web, probablemente un párrafo funcione bien y luego
podríamos cambiar su apariencia para darle los efectos visuales deseados, sin
embargo, si deseamos resaltar dicho texto sobre otros existentes, podemos usar
un encabezado para darle una jerarquía y diferenciarlo de los demás.

#### Challenge: Texto promocional

¿Cómo harías para agregar el texto promocional? ¿Te has dado cuenta que dentro
del mismo texto hay algunas palabras que tienen un mayor énfasis (formato en
_negrita_)? ¿Cómo harías para cambiar el formato de solo esas palabras?

Probablemente ya habrás pensado que existe una etiqueta para eso, no te
intimides y pregúntale a San Google (se volverá en uno de tus mejores amigos).

#### Guía: Agregando un formulario

Los formularios en HTML hacen uso de etiquetas particulares para denotar el tipo
de _control_ (caja de texto, botones, etc) que se va a usar en el formulario.

La mayoría de cajas de texto se definen con la etiqueta `<input />` y su
comportamiento por defecto depende del uso del valor de un atributo, llamado
`type`. Esta etiqueta no lleva contenido dentro de la misma, por lo que la
manera de cerrar la etiqueta es automática usando `/>` en vez de `</input>`.

El `input` más común usado en los formularios es:

```html
<input type="text" />
```

Usando este tipo de _input_, la web mostrará una caja de texto que permitirá
ingresar cualquier tipo de texto (números, letras, caracteres especiales, etc),
mientras que usando otros tipos podemos agregar algunas validaciones por defecto
que tenga el navegador. En este formulario, tenemos necesitamos obtener un
correo electrónico del usuario. Para este caso, usaremos el tipo `email`.

```html
<input type="email" />
```

Para terminar el formulario necesitamos agregar un botón, y eso lo logramos a
través de la etiqueta `<button></button>`. Debido a que el texto del botón se
pone entre las etiquetas, el cerrado de la etiqueta no es automático. Además del
texto es importante indicar el tipo de acción que realizará cuando se le de
click al botón. En este caso queremos que el formulario envíe el correo que el
usuario ingresa y por ende el tipo es a usar es `submit`.

Un detalle importante es que los controles de formulario deben estar contenidos
por una etiqueta `<form></form>`. Nuestro HTML del formulario quedaría así:

```html
<form>
  <input type="email" />
  <button type="submit">
    Try it now &rarr;
  </button>
</form>
```

Este formulario por si solo no hará ninguna acción, por el momento solo
dejaremos que esté visible, la funcionalidad la dejaremos para después.
