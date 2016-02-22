# Extending the library #

Si es necesario realizar algún cambio o está interesado en ampliar su funcionalidad con nuevos diagramas, requerirá el uso de herramientas especiales y un conocimiento más amplio.

En este apartado se explicará el proceso de empaquetado y compresión de los ficheros de código de la librería, solo debería leerlo si usted se encuentra en alguno de los siguientes supuestos:

  * Quiere añadir o eliminar algún diagrama de la librería.
  * Ha modificado el código de la librería y necesita volver a empaquetarla.

Para llevar a cabo esta tarea serán necesarias las siguientes aplicaciones:

  * [Sprockets](http://getsprockets.org/installation_and_usage)
  * [YUICompressor](http://developer.yahoo.com/yui/compressor/)
  * Empaquetado de la librería

## Important note ##

Before proceeding with the installation and use of this software, notice that the library jsUML2 is distributed under a GPL3 license. We want to improve this library, as well as write the links to those sites that make use of this software. Please, remind to contact to the project coordinator (Raúl Romero, jrromero@uco.es) and provide a link to your project if you want to let us know about your work. If you want to, we can also provide a link here.

## Sprockets ##

Sprockets (see the Installation page) has been chosen to solve dependencies among Javascript objects. Since it is not natively provided by the language, it offers a good way to analyze their dependencies and collect them all into one single file.

Sprocketize was written in Ruby, so all you need to make use of this tool is to install a recent version of this language in your computer.

## YUICompressor ##

YUICompressor is a small application that serves to compress Javascript code very significantly. As a result, it generates valid compressed files but reduced in size (around 40% less than the original).

Thos application is part of the Javascript programming library provided by Yahoo!, name YUI (_Yahoo User Interface_).


## jsUML2 packages ##

Once you have installed the preprocessing applications, you need to know how the jsUML2 packages are distributed into source directories.


```
    /src
        /core           % The library core (graphical elements and handlers, user interaction, etc.).
        /modules        % It containts UML2 elements.
            /activity   % Activity diagrams
            /class      % Class diagrams.
            /component  % Component diagrams.
            /generic    % General diagram elements (notes, lines, stereotypes, etc.)
            /profile    % Profile definition diagram and basic features
            /sequence   % Sequence diagrams.
            /stateMachine % Statechars
            /usecase    % Use case diagram.
```

When the library is packaged, it extracts information about the diagrams comprised by the 'modules' directory. So, if a developer only wants some specific diagram/s, he should add or remove this/these module directory/ies, and pack it all again.

The packaging and compression process is really simple, and a make file (called 'make.sh') is provided with the library. Notice that by executing this script, all the files comprised in the 'build' directory could be overwriten.

```
  ./make.sh
```

Once the process is finished, the package generated can be installed and used similarly to the full package provided by default. No additional procedure is required.