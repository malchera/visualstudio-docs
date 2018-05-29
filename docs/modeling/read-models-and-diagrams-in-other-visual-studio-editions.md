---
title: Read models and diagrams in other Visual Studio editions
ms.date: 11/04/2016
ms.topic: conceptual
helpviewer_keywords:
  - "models, versions of Visual Studio"
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
---
# Read models and diagrams in other Visual Studio editions
When you open a model in a version of Visual Studio that does not support model creation, the model opens in read-only mode. In this mode, you can change the layout of the diagrams, but you cannot change the model.

 To see which versions of Visual Studio support model creation, see [Version support for architecture and modeling tools](../modeling/what-s-new-for-design-in-visual-studio.md#VersionSupport).

## Obtaining Access to a Model and Diagrams
 To read a dependency diagram, you must first use Visual Studio to open the modeling project, and then open the diagram within it.

 For this reason, if you want to read a dependency diagram, you must also have access to the modeling project in which it was created. You can do this either by accessing the project from [!INCLUDE[esprscc](../code-quality/includes/esprscc_md.md)], or by obtaining a copy of the project files.

> [!NOTE]
>  This does not apply to code maps and .NET class diagrams generated from code. Those diagrams can be viewed independently of a modeling project.

 To read a dependency diagram, the minimum set of files that you need is as follows:

-   The two diagram files for the diagram that you want to read, for example, **MyDiagram.classdiagram and MyDiagram.classdiagram.layout**.

    > [!NOTE]
    >  For dependency diagrams, you should also have the file that is named *MyDiagram***.layerdiagram.suppressions**.

-   The modeling project file (**MyModel.modelproj**)

-   The root model file (**ModelDefinition\MyModel.uml**)

-   The package files for any package referenced in the diagram (**ModelDefinition\MyPackage.uml**)

## Changes that you can Make in Read-Only Mode
 If you open a model and its diagrams in a version of Visual Studio that does not support model creation, you cannot change the model. That is, you cannot change the elements and relationships that are displayed on the diagrams or in the model explorer. However, you can make some changes to the layout of the diagrams:

-   Rearrange the shapes and connectors on the diagram.

-   Expand and collapse shapes.

 You can save these changes. If you want to make your changes visible to other users, you must at least send the updated **.layout** files.

##  <a name="RelatedTopics"></a> Related Topics

|Title|Description|
|-----------|-----------------|
|[Dependency Diagrams: Reference](../modeling/layer-diagrams-reference.md)|A layer diagram shows the structure of an existing or proposed architecture. When code is written, it can be automatically validated against a layer diagram.|

## See Also

- [Create models for your app](../modeling/create-models-for-your-app.md)