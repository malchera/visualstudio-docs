---
title: "Sample Excel Extension: PropertyProvider Class"
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
# Sample Excel Extension: PropertyProvider Class
This internal class extends the <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider> class and provides property services for [!INCLUDE[ofprexcel](../test/includes/ofprexcel_md.md)] elements to record and play back user interface (UI) tests.

## GetControlSupportLevel Method
 The <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider.GetControlSupportLevel%2A> method returns a number that indicates the level of support that the property provider can offer for the provided control. The higher the returned value, the more the property provider can support the control. In this case, the method checks the value of the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.TechnologyName%2A> property of the provided control. If the value is "Excel" and if the <xref:Microsoft.VisualStudio.TestTools.UITest.Extension.IUITechnologyElement.ControlTypeName%2A> indicates it is a `CellElement`, the method returns the highest value; otherwise, it returns zero, which indicates that no support is provided.

## GetPropertyNames Method
 Returns a dictionary of property names and property descriptors for the supported properties of an Excel Cell control.

## GetPropertyDescriptor Method
 This method is called by the testing framework to get the predefined property descriptor for the provided property name.

## GetPropertyValue and SetPropertyValue Methods
 The `GetPropertyValue` method uses the `Communicator` class of this extension to return the property value from Excel. The `SetPropertyValue` method uses the <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard> class and the `Communicator` component to set the property value. These methods are called by the testing framework.

## Code Generation Customization Methods
 These methods are not implemented for this extension. Therefore, they either return `null` or throw the <xref:System.NotImplementedException>.

## See also

- <xref:Microsoft.VisualStudio.TestTools.UITesting.UITestPropertyProvider>
- <xref:Microsoft.VisualStudio.TestTools.UITesting.Keyboard>
- [Extending Coded UI Tests and Action Recordings to Support Microsoft Excel](../test/extending-coded-ui-tests-and-action-recordings-to-support-microsoft-excel.md)
