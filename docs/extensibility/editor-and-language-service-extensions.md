---
title: "Editor and Language Service Extensions | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: 
  - "vs-ide-sdk"
ms.topic: "conceptual"
helpviewer_keywords: 
  - "editors [Visual Studio SDK]"
ms.assetid: 5653bac9-724f-4948-a820-68ce6aa96365
author: "gregvanl"
ms.author: "gregvanl"
manager: douge
ms.workload: 
  - "vssdk"
---
# Editor and Language Service Extensions
You can extend most features of the Visual Studio code editor. The editor is based on the Windows Presentation Foundation (WPF) and is written in managed code. Although this design differs from the designs in earlier versions of Visual Studio, it provides most of the same features. To extend the editor, use the Managed Extensibility Framework (MEF).  
  
 The Visual Studio SDK provides adapters known as *shims* to support VSPackages that were written for earlier versions. Nevertheless, if you have an existing VSPackage, we recommend that you update it to the new technology to obtain better performance and reliability.  
  
## Related Topics  
  
|Title|Description|  
|-----------|-----------------|  
|[Creating an Extension with an Editor Item Template](../extensibility/creating-an-extension-with-an-editor-item-template.md)|Introduction to using the Editor item templates.|  
|[Extending the Editor and Language Services](../extensibility/extending-the-editor-and-language-services.md)|Links to documents that introduce the design and features of the core editor and show how to extend it.|  
|[Legacy Interfaces in the Editor](../extensibility/legacy-interfaces-in-the-editor.md)|Links to documents that explain how to access the core editor from existing code.|  
|[Creating Custom Editors and Designers](../extensibility/creating-custom-editors-and-designers.md)|Links to documents that explain how to create custom editors.|  
|[Legacy Language Service Extensibility](../extensibility/internals/legacy-language-service-extensibility.md)|Links to documents that describe how to integrate programming languages into Visual Studio.|  
|[Managed Extensibility Framework (MEF)](/dotnet/framework/mef/index)|Introduces the Managed Extensibility Framework (MEF).|  
|[Windows Presentation Foundation](/dotnet/framework/wpf/index)|Introduces the Windows Presentation Foundation (WPF).|