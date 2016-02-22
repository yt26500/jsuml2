We will list here the most important updates to the jsUML2 package.

# RELEASE 004 #

  * Code errors fixed.
  * New UML diagrams added:
    * Object/instance diagrams.
    * Package diagrams.
    * Deployment diagrams.
  * Several new UML elements added to existing diagrams.
  * Style customization extended.
  * Profiling improved.
  * Event handling for mobile devices and responsive devices.

### Detailed information ###

  * Modifications all around the code to fix errors.
  * Event handling modified to consider touch-screen interfaces.
  * Style features extended.
  * _Core layer_:
    * Modules added: Cube, PropertyItem, PropertyFields, InstanceItem, ArtifactSymbol, ArtifactItem, ArtifactFields, CubeFigure
    * Modules edited: NodeFigure, Node, Relation, RelationLine, RelationEnd, Diagram, Component, TextFields, CollapsibleFields, Text, AttributeItem

  * _UML layer_:
    * Activity module (edited): Object, AcceptEventAction, ConnectorActivity, DataStore, Decision\_MergeNode, ExceptionHandler, ExpansionNode, Flow, FlowFinal, HierarchicalSwimlane, NodeAction, ObjectActivity, Pin, SendSignalAction, Swimlane, TimeEvent
    * Class module (added): NAssociation, Link, Instance
    * Class module (edited): Association, Class, ComponentElement, Composition, Dependency, Generalization, GeneralizationSet, Package, PackageContainer, Realization
    * Component module (edited): InterfaceExtended, NodeInterface, NodePorts, GeneralizationSet, Dependency, Association, InterfaceUse, NAssociation, Realization
    * Usecase module (added): UseCaseClassifier
    * Usecase module (edited): UseCaseExtended, GeneralizationSet
    * Package module added
    * Deployment module added
  * _Application layer_ (demo):
    * New diagrams (instance, deployment, package) added.
    * Updated reflected.