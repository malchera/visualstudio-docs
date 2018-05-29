---
title: "Workflow Designer - Legacy Workflow Activities"
ms.date: 01/18/2017
ms.topic: reference
ms.prod: visual-studio-dev15
ms.technology: vs-workflow-designer
helpviewer_keywords:
  - "workflows, activities"
  - "activities"
  - "workflow activities"
ms.assetid: 4af7a06b-1e82-43c8-aec8-0dc5fb63d08a
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# Legacy Workflow Activities

Windows Workflow Foundation (WF) includes a default set of activities that provide functionality for control flow, conditions, event handling, state management, and communicating with applications and services. When designing workflows, you can use the system-provided activities that are provided by the Windows Workflow Designer, or you can create your own custom activities.

The following table lists the Windows Workflow Foundation framework out-of-box activity set. Many, but not all, of these activities are represented by activity designers that can be accessed from the **Toolbox** of the Workflow Designer. To create an activity, drag its designer from the **Toolbox** and drop it on the design surface.

|Activity|Description|
|--------------|-----------------|
|<xref:System.Workflow.Activities.CallExternalMethodActivity>|Used with the **HandleExternalEventActivity** activity for input and output communications with a local service. For more information, see [Using the CallExternalMethodActivity Activity](http://go.microsoft.com/fwlink?LinkID=65060).|
|**System.Workflow.Activities.CancellationHandlerActivity**|Used to contain cleanup logic for a composite activity canceled before all the composite activity's children are finished executing. For more information, see [Using the CancellationHandlerActivity Activity](http://go.microsoft.com/fwlink?LinkID=65061).|
|<xref:System.Workflow.Activities.CodeActivity>|Enables you to add Visual Basic or C# code to your workflow. For more information, see [Using the CodeActivity Activity](http://go.microsoft.com/fwlink?LinkID=65062).|
|<xref:System.Workflow.Activities.CompensatableSequenceActivity>|A compensatable version of <xref:System.Workflow.Activities.SequenceActivity>. For more information, see [Using the CompensatableSequenceActivity Activity](http://go.microsoft.com/fwlink?LinkID=65002).|
|**System.Workflow.Activities.CompensatableTransactionScopeActivity**|A compensatable version of **TransactionScopeActivity**. For more information, see [Using the CompensatableTransactionScopeActivity Activity](http://go.microsoft.com/fwlink?LinkID=65063).|
|**System.Workflow.Activities.CompensateActivity**|Enables you to call code to undo or to compensate for operations already performed by the workflow when an error occurs. For more information, see [Using the CompensateActivity Activity](http://go.microsoft.com/fwlink?LinkID=65064).|
|**System.Workflow.Activities.CompensationHandlerActivity**|A wrapper for one or more activities that perform compensation for a completed TransactionScopeActivity activity For more information, see [Using the CompensationHandlerActivity Activity](http://go.microsoft.com/fwlink?LinkID=65065).|
|<xref:System.Workflow.Activities.ConditionedActivityGroup>|Executes child activities based on a condition that applies to the <xref:System.Workflow.Activities.ConditionedActivityGroup> activity itself and based on conditions that apply separately to each child. For more information, see [Using the ConditionedActivityGroup Activity](http://go.microsoft.com/fwlink?LinkID=65066).|
|<xref:System.Workflow.Activities.DelayActivity>|Enables you to build delays in your workflow that are based on a time-out interval. For more information, see [Using the DelayActivity Activity](http://go.microsoft.com/fwlink?LinkID=65067).|
|<xref:System.Workflow.Activities.EventDrivenActivity>|Wraps one or more activities that are executed when a specified event occurs. For more information, see [Using the EventDrivenActivity Activity](http://go.microsoft.com/fwlink?LinkID=65068).|
|<xref:System.Workflow.Activities.EventHandlersActivity>|Provides a framework for associating events with an activity. For more information, see [Using the EventHandlersActivity Activity](http://go.microsoft.com/fwlink?LinkID=65069).|
|<xref:System.Workflow.Activities.EventHandlingScopeActivity>|Executes its main child activity concurrently with an <xref:System.Workflow.Activities.EventHandlersActivity>. For more information, see [Using the EventHandlingScopeActivity Activity](http://go.microsoft.com/fwlink?LinkID=65070).|
|**System.Workflow.Activities.FaultHandlerActivity**|Used to handle an exception of a type that you specify. For more information, see [Using the FaultHandlerActivity Activity](http://go.microsoft.com/fwlink?LinkID=65071).|
|**System.Workflow.Activities.FaultHandlersActivity**|Represents a composite activity that has an ordered list of child activities of type **System.Workflow.Activities.FaultHandlerActivity**. For more information, see [Using the FaultHandlersActivity Activity](http://go.microsoft.com/fwlink?LinkID=65072).|
|<xref:System.Workflow.Activities.HandleExternalEventActivity>|Used in conjunction with the <xref:System.Workflow.Activities.CallExternalMethodActivity> activity for input and output communications with a local service. For more information, see [Using the HandleExternalEventActivity Activity](http://go.microsoft.com/fwlink?LinkID=65073).|
|<xref:System.Workflow.Activities.IfElseActivity>|Tests a condition on each branch and performs activities on the first branch for which the condition equals **true**. For more information, see [Using the IfElseActivity Activity](http://go.microsoft.com/fwlink?LinkID=65074).|
|<xref:System.Workflow.Activities.IfElseBranchActivity>|Represents a branch of an <xref:System.Workflow.Activities.IfElseActivity>. For more information, see [Using the IfElseBranchActivity Activity](http://go.microsoft.com/fwlink?LinkID=65075).|
|<xref:System.Workflow.Activities.InvokeWebServiceActivity>|Enables your workflow to invoke a Web service. For more information, see [Using the InvokeWebServiceActivity Activity](http://go.microsoft.com/fwlink?LinkID=65076).|
|<xref:System.Workflow.Activities.InvokeWorkflowActivity>|Enables your workflow to invoke another workflow. For more information, see [Using the InvokeWorkflowActivity Activity](http://go.microsoft.com/fwlink?LinkID=65077).|
|<xref:System.Workflow.Activities.ListenActivity>|A composite activity that contains only <xref:System.Workflow.Activities.EventDrivenActivity> child activities. For more information, see [Using the ListenActivity Activity](http://go.microsoft.com/fwlink?LinkID=65078).|
|<xref:System.Workflow.Activities.ParallelActivity>|Provides a way to schedule two or more child **SequenceActivity** activity branches for processing at the same time. For more information, see [Using the ParallelActivity Activity](http://go.microsoft.com/fwlink?LinkID=65079).|
|<xref:System.Workflow.Activities.PolicyActivity>|Use to represent a collection of rules. A rule consists of conditions and resulting actions. For more information, see [Using the PolicyActivity Activity](http://go.microsoft.com/fwlink?LinkID=65004).|
|<xref:System.Workflow.Activities.ReplicatorActivity>|Creates multiple instances of a single child activity. For more information, see [Using the ReplicatorActivity Activity](http://go.microsoft.com/fwlink?LinkID=65080).|
|<xref:System.Workflow.Activities.SequenceActivity>|Provides a simple way to link multiple activities together for sequential execution. For more information, see [Using the SequenceActivity Activity](http://go.microsoft.com/fwlink?LinkID=65081).|
|<xref:System.Workflow.Activities.SetStateActivity>|Specifies a transition to a new state. For more information, see [Using the SetStateActivity Activity](http://go.microsoft.com/fwlink?LinkID=65082).|
|<xref:System.Workflow.Activities.StateActivity>|Represents a state in a state machine workflow. For more information, see [Using the StateActivity Activity](http://go.microsoft.com/fwlink?LinkID=65083).|
|<xref:System.Workflow.Activities.StateFinalizationActivity>|Used in a <xref:System.Workflow.Activities.StateActivity> activity as a container for child activities that are executed when leaving the **StateActivity** activity. For more information, see [Using the StateFinalizationActivity Activity](http://go.microsoft.com/fwlink?LinkID=65008).|
|<xref:System.Workflow.Activities.StateInitializationActivity>|Used in a <xref:System.Workflow.Activities.StateActivity> activity as a container for child activities that are executed when entering the **StateActivity** activity. For more information, see [Using the StateInitializationActivity Activity](http://go.microsoft.com/fwlink?LinkID=65006).|
|**System.Workflow.Activities.SuspendActivity**|Suspends the operation of your workflow to enable intervention in the event of some error condition that requires special attention. For more information, see [Using the SuspendActivity Activity](http://go.microsoft.com/fwlink?LinkID=65084).|
|**System.Workflow.Activities.SynchronizationScopeActivity**|Executes contained activities sequentially in a synchronized domain. For more information, see [Using the SynchronizationScopeActivity Activity](http://go.microsoft.com/fwlink?LinkID=65085).|
|**System.Workflow.Activities.TerminateActivity**|Enables you to immediately end the operation of your workflow in the event of an error condition. For more information, see [Using the TerminateActivity Activity](http://go.microsoft.com/fwlink?LinkID=65086).|
|**System.Workflow.Activities.ThrowActivity**|Enables you to capture business exceptions thrown as part of the process metadata for a workflow. For more information, see [Using the ThrowActivity Activity](http://go.microsoft.com/fwlink?LinkID=65087).|
|**System.Workflow.Activities.TransactionScopeActivity**|Provides a framework for transactions and exception handling. For more information, see [Using the TransactionScopeActivity Activity](http://go.microsoft.com/fwlink?LinkID=65088).|
|<xref:System.Workflow.Activities.WebServiceFaultActivity>|Enables you to model the occurrence of a Web service fault. For more information, see [Using the WebServiceFaultActivity Activity](http://go.microsoft.com/fwlink?LinkID=65089).|
|<xref:System.Workflow.Activities.WebServiceInputActivity>|Receives data from a Web service. For more information, see [Using the WebServiceInputActivity Activity](http://go.microsoft.com/fwlink?LinkID=65090).|
|<xref:System.Workflow.Activities.WebServiceOutputActivity>|Responds to a Web service request made to a workflow. For more information, see [Using the WebServiceOutputActivity Activity](http://go.microsoft.com/fwlink?LinkID=65092).|
|<xref:System.Workflow.Activities.WhileActivity>|Enables your workflow to loop until a condition is met. For more information, see [Using the WhileActivity Activity](http://go.microsoft.com/fwlink?LinkID=65091).|

For more information about how to create custom activities, see [Developing Custom Activities](http://go.microsoft.com/fwlink?LinkID=65023) and [Using the Legacy Activity Designer](../workflow-designer/using-the-legacy-activity-designer.md).

## See also

- [Windows Workflow Foundation Activities](http://go.microsoft.com/fwlink?LinkID=65005)
- [Developing Workflows](http://go.microsoft.com/fwlink?LinkID=65010)
- [Developing Workflow Activities](http://go.microsoft.com/fwlink?LinkID=65023)