# Library architecture #

This is a layered library architecture. Graphics handlers, UML-specific objects and application objects are separated in layers.

  * 'UDCore': This is the library core, and concentrates most of the functional capabilities, and complexity. It is thought to a wide range of tasks: drawing lines and shapes, handling of user events (interaction), etc.

  * 'UDModules': The middle layer. This contains the UML2 objects, as required by the Standard, implemented on the 'UDCore' layer.

The uppest layer should be implemented by the programmer. Here we provide a sample simple UML editor, as a proof-of-concept. This is the nearest layer to the user, and should be implemented on the 'UDModules' layer.

Para descargar la guía de referencia:
<Enlace a quickreference.pdf>

## Quick overview ##

Supported UML objects:

  * UDCore
    * Diagram
    * Node
    * Relation

  * UDModules
    * Use case diagram:
      * Use case diagram
      * Actor
      * Use case
      * Extended use case
      * System
      * Subsystem
      * Relationships:
        * Communication
        * Extend
        * Include
        * Generalization

  * Class diagrams
    * Class diagram
    * Package
    * Package (container)
    * Class
    * Component
    * Interface
    * Relationships:
      * Aggregation
      * Association
      * Composition
      * Dependency
      * Generalization
      * Realization
      * Use
      * Combination
      * Public package import
      * Private package import

  * Component diagrams
    * Component diagram
    * Component
    * Interface
    * Port
    * (Specific) relationships
      * Use
      * Realize


  * Message sequence diagrams:
    * MSC diagram
    * Lifeline
    * Interactions:
      * Call message
      * Send message
      * Reply message
      * Create
      * Delete / destroy
    * Blocks:
      * OPTion
      * ALTernative
      * LOOP
      * BREAK

  * State charts:
    * State machine diagram
    * Simple state
    * Composite state
    * Initial pseudostate
    * Final pseudostate
    * Entry point
    * Exit point
    * Junction
    * Vertical region
    * Horizontal region
    * Transition


  * Módulo de objetos genéricos
    * Nota
    * Línea simple