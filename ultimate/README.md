
Descargar
--------

[Markdown 1.0.1] [dl] (18 KB) - 17 de diciembre de 2004

[dl]: http://daringfireball.net/projects/downloads/Markdown_1.0.1.zip


Introducción
------------

Markdown es una herramienta de conversión de texto a HTML para escritores web. Reducción
le permite escribir utilizando un texto sin formato fácil de leer y escribir
formatee, luego conviértalo a XHTML (o HTML) estructuralmente válido.

Por lo tanto, "Markdown" es dos cosas: (1) una sintaxis de formato de texto sin formato;
y (2) una herramienta de software, escrita en Perl, que convierte el texto sin formato
formato a HTML. Consulte la página [Sintaxis] [] para obtener detalles sobre
Sintaxis de formato de Markdown. Puedes probarlo, ahora mismo, usando el
en línea [Dingus] [].

  [sintaxis]: / projects / markdown / syntax
  [dingus]: / projects / markdown / dingus

El objetivo primordial de diseño para la sintaxis de formato de Markdown es hacer
Es lo más legible posible. La idea es que un Markdown formateado
El documento debe ser publicable como está, como texto sin formato, sin mirar.
Como si estuviera marcado con etiquetas o instrucciones de formato. Mientras
La sintaxis de Markdown ha sido influenciada por varios textos existentes a HTML
Filtros, la mayor fuente de inspiración para Markdown's.
La sintaxis es el formato del correo electrónico de texto plano.

La mejor manera de familiarizarse con la sintaxis de formato de Markdown es simplemente
para ver un documento con formato Markdown. Por ejemplo, puedes ver
La fuente de Markdown para el texto del artículo en esta página aquí:
<http://daringfireball.net/projects/markdown/index.text>

(Puede usar este truco de sufijo '.text' para ver la fuente de Markdown para
el contenido de cada una de las páginas de esta sección, p. ej. la
Páginas [Sintaxis] [s_src] y [Licencia] [l_src].)

  [s_src]: /projects/markdown/syntax.text
  [l_src]: /projects/markdown/license.text

Markdown es software libre, disponible en una fuente abierta de estilo BSD
licencia. Consulte la página [Licencia] [pl] para obtener más información.

  [pl]: / projects / markdown / license


Lista de discusión <a id="discussion-list" />
---------------

He configurado una lista de correo pública para discusión sobre Markdown [ml].
Cualquier tema relacionado con Markdown, tanto su sintaxis de formato como
Su software - es un juego justo para la discusión. Cualquiera que este interesado
es bienvenido a unirse.

Espero que la lista de correo genere buenas ideas para el futuro.
Mejoras en Markdown.

  [ml]: http://six.pairlist.net/mailman/listinfo/markdown-discuss


Instalación y requisitos <a id="install" />
-----------------------------

Markdown requiere Perl 5.6.0 o posterior. Bienvenidos al siglo XXI.
Markdown también requiere el módulo de biblioteca Perl estándar [Digest :: MD5]
[md5], que probablemente ya esté instalado en su servidor.

  [md5]: http://search.cpan.org/dist/Digest-MD5/MD5.pm


### Tipos móviles ###

Markdown funciona con Movable Type versión 2.6 o posterior (incluyendo
Tipo móvil 3.0).

1. Copie el archivo "Markdown.pl" en sus "complementos" de Movable Type
directorio. El directorio de "complementos" debe estar en el mismo directorio
como "mt.cgi"; si el directorio de "complementos" no existe, use
Tu programa FTP para crearlo. Su instalación debe verse como
esta:

        (mt home) /plugins/Markdown.pl

2. Una vez instalado, Markdown aparecerá como una opción en Movable Type
Menú emergente de formato de texto. Esto es seleccionable en una base por post:

! [Captura de pantalla del menú 'Formato de texto' de Movable Type] [tfmenu]

Markdown traduce tus publicaciones a HTML cuando publicas; los mensajes
ellos mismos se almacenan en su base de datos de MT en formato Markdown.

3. Si también instala SmartyPants 1.5 (o posterior), Markdown
ofrece una segunda opción de formato de texto: "Markdown With
SmartyPants ". Esta opción es la misma que la normal" Markdown "
formateador, excepto que utiliza automáticamente SmartyPants para crear
Corregir de forma tipográfica las comillas, los guiones y los puntos suspensivos. Ver
la [página web de SmartyPants] [sp] para más información.

4. Para que Markdown (o "Markdown With SmartyPants") sea su valor predeterminado
Opción de formato de texto para nuevas publicaciones, vaya a Configuración de weblog:
Preferencias.

Tenga en cuenta que, de forma predeterminada, Markdown produce una salida XHTML. Para configurar
Markdown para producir una salida HTML 4, consulte "Configuración", a continuación.

  [sp]: http://daringfireball.net/projects/smartypants/



### Blosxom ###

Markdown funciona con la versión Blosxom 2.0 o posterior.

1. Cambie el nombre del complemento "Markdown.pl" a "Markdown" (el caso es
    importante). Movable Type requiere que los complementos tengan un ".pl"
    extensión; Blosxom lo prohíbe.

2. Copie el archivo de plug-in "Markdown" en su carpeta de plug-ins de Blosxom.
    Si no está seguro de dónde está la carpeta de complementos de Blosxom, consulte la
    Documentación de Blosxom para información.

3. Eso es todo. Las entradas en tu weblog ahora serán automáticamente.
procesado por Markdown.

4. Si desea aplicar el formato Markdown solo a ciertos
mensajes, en lugar de todos ellos, Markdown puede ser opcionalmente utilizado en
junto con el complemento [Meta] [] de Blosxom. Primero, instale el
Meta plug-in. A continuación, abra el archivo del complemento Markdown en un texto
editor, y establecer la variable de configuración `$ g_blosxom_use_meta`
a 1. Luego, simplemente incluya una línea de encabezado "` meta-markup: Markdown` "
En la parte superior de cada publicación, compones usando Markdown.

  [meta]: http://www.blosxom.com/plugins/meta/meta.htm


### BBEdit ###

Markdown funciona con BBEdit 6.1 o posterior en Mac OS X. También funciona
con BBEdit 5.1 o posterior y MacPerl 5.6.1 en Mac OS 8.6 o posterior. Si
está ejecutando Mac OS X 10.2 (Jaguar), puede que necesite instalar el
Módulo Perl [Digest :: MD5] [md5] de CPAN; Digest :: viene el MD5
preinstalado en Mac OS X 10.3 (Panther).

1. Copie el archivo "Markdown.pl" en la carpeta de filtros apropiada en su
Carpeta "BBEdit Support". En Mac OS X, esto debería ser:

        Soporte BBEdit / Soporte Unix / Filtros Unix /

    Consulte la documentación de BBEdit para obtener más detalles sobre la ubicación de
    estas carpetas

    Puede cambiar el nombre de "Markdown.pl" a lo que desee.

2. Eso es todo. Para usar Markdown, seleccione un texto en un documento BBEdit,
luego elija Markdown en el submenú Filtros en "#!" menú, o
la paleta flotante de los filtros



Configuración <a id="configuration"> </a>
-------------

De forma predeterminada, Markdown produce una salida XHTML para etiquetas con elementos vacíos.
P.ej.:

    <br />

Markdown se puede configurar para producir etiquetas de estilo HTML; p.ej.:

    <br>


### Tipos móviles ###

Necesitas usar una etiqueta especial de contenedor `MTMarkdownOptions` en cada
Plantilla de tipo móvil en la que desea una salida de estilo HTML 4:

    <MTMarkdownOptions output = 'html4'>
        ... pon tu contenido de entrada aquí ...
    </MTMarkdownOptions>

La forma más fácil de usar MTMarkdownOptions es probablemente poner el
etiqueta de apertura justo después de su etiqueta `<body>`, y la etiqueta de cierre derecha
antes de `</body>`.

Para suprimir el procesamiento de Markdown en una plantilla en particular, es decir, para
publicar el texto sin formato de Markdown sin traducción en
(X) HTML, establece el atributo `output` en 'raw':

    <MTMarkdownOptions output = 'raw'>
        ... pon tu contenido de entrada aquí ...
    </MTMarkdownOptions>


### Línea de comando ###

Use el interruptor de línea de comandos `--html4tags` para producir un resultado HTML desde un
Línea de comando de estilo Unix. P.ej.:

    % perl Markdown.pl --html4tags foo.text

Escriba `perldoc Markdown.pl`, o lea la documentación de POD en el
Código fuente Markdown.pl para más información.


Agradecimientos <a id="acknowledgements" />
----------------

[Aaron Swartz] [] merece una enorme cantidad de crédito por sus comentarios sobre el
Diseño de la sintaxis de formato de Markdown. Markdown es * mucho * mejor gracias
a las ideas, comentarios y pruebas de Aaron. Además, Aaron's [html2text] []
es una utilidad muy útil (y gratuita) para convertir HTML en
Texto sin formato en formato markdown.

[Nathaniel Irons] [], [Dan Benjamin] [], [Daniel Bogan] [], y [Jason Perkins] []
También merecen las gracias por sus comentarios.

[Michel Fortin] [] ha portado Markdown a PHP; es un puerto espléndido, y muy recomendable para cualquiera que busque una implementación PHP de Markdown.

  [Aaron Swartz]: http://www.aaronsw.com/
  [Nathaniel Irons]: http://bumppo.net/
  [Dan Benjamin]: http://hivelogic.com/
  [Daniel Bogan]: http://waferbaby.com/
  [Jason Perkins]: http://pressedpants.com/
  [Michel Fortin]: http://www.michelf.com/projects/php-markdown/
  [html2text]: http://www.aaronsw.com/2002/html2text/
 
  [tfmenu]: /graphics/markdown/mt_textformat_menu.png
