# Installing the library #
To fully understand the installation process of this library, you need to know how its packages are organized:

  * 'UDCore': This is the lowest level, core package. It concentrates most of the drawing functionalities. Actually, this layer is in charge of drawing lines and shapes, handling objects and defining the user interaction.

  * 'UDModules': This is the middle level package. It defines the UML2 objects using the features provided by the lowest layer, according to the standard.

  * The application layer might be the uppest layer. This layer should be built by the programmer following his own requirements. Only as an example of this layer, we provide the jsUML2 editor, which is built on the top of the 'UDModules' layer.

# Deployment #

The library comprise a large number of object files, also including some minonitary style sheet and image file. However, if you want to make use of the library, it is recommended to minimize this number of files, leaving only those related to the UML elements that you want to use.

jsUML2 is packaged and compressed into two Javascript files, a common style sheet and a directory for image files. All the files to be distributed to the end user are generated in a directory named 'build'. Its structure is the following:

```
    /build
        /css         % Style sheets
        /img         % Image files required by the top application
        /temp        % Javascript files (no compressed)
        UDCore.js    % Packaged and compressed Javascript file for the lowest layer
        UDModules.js % Package and compressed Javascript file for the middle layer
```

Directories 'css', 'img', and both 'UDCore.js' and 'UDModules.js' files should be created in that form to keep the library in working order. The temporary directory (named 'temp') contains the working js files without comprising to be used just in case they need to be debugged or refined. Nevertheless, they can usually be removed.

Next, you need to add the labels that link your application to the library source code and style sheet, inside the HTML document header. You may use the labels `<head></head>`.

```
    <link type="text/css" rel="stylesheet" 
          href="css/UDStyle.css" media="screen" />
    <script type="text/javascript" src="UDCore.js"></script>
    <script type="text/javascript" src="UDModules.js"></script>
```

By default, the path of these files should be pointed to the application root. Notice that it is important to, first of all, properly link the file 'UDCore.js'. Any other file will depend on this one. Next, a linking label to 'UDModules.js' has to be included. This order will minimize the appareance of dependency issues.



# Building files #

If you want to build the code, you may require the following tools.

### Sprocketize ###

This tool serves to solve the existing dependences among the different javascript files.

Sprocketize can be reached from http://getsprockets.org

Run the following command to download:

"gem --install remote sprockets"

Notice that Gem Ruby needs to be installed first.

### YIU Compressor ###

Yui Compressor is a tool from the Yahoo Javascript API that help us to compress the javascript code and, in consequence, it can significantly reduce the size of these files.

Further information about Yui Compressor is available from http://developer.yahoo.com/yui/compressor/

or can be downloaded at
http://yuilibrary.com/downloads/#yuicompressor

YUICompressor 2.4.2 is included in this package, named yuicompressor.jar. All you need to run it is to ensure that the Java VM (JRE) is properly installed in your system.