---
title: "Workflow Designer - Delay Activity Designer"
ms.date: 11/04/2016
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
f1_keywords:
  - "System.Activities.Statements.Delay.UI"
ms.assetid: f51742a8-2c9a-47d1-8a23-18459d03ae19
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# Delay Activity Designer

The **Delay** activity designer is used to create and configure a <xref:System.Activities.Statements.Delay> activity.

## The Delay Activity

The <xref:System.Activities.Statements.Delay> activity delays the execution of a workflow for a specified amount of time.

### Using the Delay Activity Designer

The **Delay** activity designer can be found in the **Primitives** category of the **Toolbox**, which is accessed by clicking the **Toolbox** tab of the Workflow Designer (Alternatively, select **Toolbar** from the **View** menu, or CTRL+ALT+X.)

The **Delay** activity designer can be dragged from the **Toolbox** and dropped on to the Workflow Designer surface wherever activities are usually placed, such as inside a <xref:System.Activities.Statements.Sequence>. This creates a <xref:System.Activities.Statements.Delay> activity with a default <xref:System.Activities.Activity.DisplayName%2A> of Delay. The <xref:System.Activities.Activity.DisplayName%2A> can be edited in the header of the **Delay** activity designer or in the **DisplayName** box of the property grid.

### The Delay Properties

The following table shows the <xref:System.Activities.Statements.Delay> properties and describes how they are used in the designer. These properties can be edited in property grid and of them some can be edited on Workflow Designerdesigner surface.

|Property Name|Required|Usage|
|-------------------|--------------|-----------|
|<xref:System.Activities.Activity.DisplayName%2A>|False|The friendly name of the <xref:System.Activities.Statements.Delay> activity. The default is Delay. Although the <xref:System.Activities.Activity.DisplayName%2A> value is not strictly required, it is a best practice to use one.|
|<xref:System.Activities.Statements.Delay.Duration%2A>|True|The amount of time to delay the workflow. This property is set in the property grid. Type in either a literal <xref:System.TimeSpan> in the format 00:00:00 or a Visual Basic expression to specify the amount of time.|

## See also

- [Primitives](../workflow-designer/primitives-activity-designers.md)
- [Assign](../workflow-designer/assign-activity-designer.md)
- [Delay Activity Designer](../workflow-designer/delay-activity-designer.md)
- [InvokeMethod](../workflow-designer/invokemethod-activity-designer.md)
- [WriteLine](../workflow-designer/writeline-activity-designer.md)