---
title: "Document Position | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: 
  - "vs-ide-sdk"
ms.topic: "conceptual"
helpviewer_keywords: 
  - "debugging [Debugging SDK], contexts"
ms.assetid: b59d739c-7572-427f-a70d-4e5df63d02c1
author: "gregvanl"
ms.author: "gregvanl"
manager: douge
ms.workload: 
  - "vssdk"
---
# Document Position
In [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] debugging, a **document position**:  
  
-   Provides an abstraction of a position in a source file as known to the IDE. For most languages today, a document position can be thought of as a position in a source file.  
  
-   Describes a position in a source document to a debug engine.  
  
-   Is implemented by an [IDebugDocumentPosition2](../../extensibility/debugger/reference/idebugdocumentposition2.md) interface.  
  
## See Also  
 [Code Context](../../extensibility/debugger/code-context.md)   
 [Document Context](../../extensibility/debugger/document-context.md)   
 [Symbol Provider](../../extensibility/debugger/symbol-provider.md)   
 [Symbol Provider Interfaces](../../extensibility/debugger/reference/symbol-provider-interfaces.md)   
 [Debugger Contexts](../../extensibility/debugger/debugger-contexts.md)