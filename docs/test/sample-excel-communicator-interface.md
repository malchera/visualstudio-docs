---
title: "Sample Excel Communicator Interface"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: sample
ms.author: gewarren
manager: douge
ms.workload: 
  - "multiple"
author: gewarren
---
# Sample Excel Communicator Interface
The sample `IExcelUICommunication` interface is used in the `ExcelUICommunicator` object in the `ExcelAddIn` project.

## IExcelUICommunication Interface
 This interface defines the communication points between the `CodedUIExtension`, which runs in the Coded UI Test process, and the `ExcelCodedUIAddIn`, which runs in the [!INCLUDE[ofprexcel](../test/includes/ofprexcel_md.md)] process.

 The `ExcelCodedUIAddinHelper` assembly has a `ExcelUICommunicator` class that derives from this interface and uses the Excel object model to process the methods.

 Some methods get the requested information from Excel then create and return one of the information objects, such as the `CellInformation` object.

 Other methods use a provided information object, find the corresponding control in Excel, and perform some process on the control. For example, the `ScrollIntoView` method scrolls the Worksheet so that the designated cell is visible.

## CodedUIExtensibilitySample and ExcelCodedUIAddinHelper Communication
 The `ExcelCodedUIAddinHelper` assembly runs in the Excel process and has the `UICommunicator` class that implements the `IExcelUITestCommunication` interface and gets or sets the required information directly from the Excel UI.

 The `CodedUIExtensibilitySample` assembly runs in the Visual Studio Coded UI Test process. This assembly has the `Communicator` class that opens a .NET Remoting channel, and provides an `Instance` property that uses the `IExcelUICommunication` interface to use the `UICommunicator` object in the `ExcelCodedUIAddinHelper` assembly to pass requests and information objects, such as a `CellInformation` object, back and forth between the two assemblies.

## See also

- [Extending Coded UI Tests and Action Recordings to Support Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)
- [Sample Excel Add-In for Coded UI Testing](../test/sample-excel-add-in-for-coded-ui-testing.md)
- [Sample Coded UI Test Extension for Excel](../test/sample-coded-ui-test-extension-for-excel.md)
