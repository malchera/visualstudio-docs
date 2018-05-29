---
title: "Create custom views of managed objects | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: "vs-ide-debug"
ms.topic: "conceptual"
f1_keywords: 
  - "vs.debug.data.elements"
dev_langs: 
  - "CSharp"
  - "VB"
  - "FSharp"
  - "C++"
helpviewer_keywords: 
  - "data types [C#], custom"
  - "custom data types"
  - "managed code, custom data types"
  - "autoexp.dat file"
  - "mcee_cs.dat file"
  - "debugger, expanding data types"
  - "mcee_mc.dat file"
ms.assetid: 9969e9b2-9008-4729-8a14-0d6deaa61576
author: "mikejo5000"
ms.author: "mikejo"
manager: douge
ms.workload: 
  - "dotnet"
---
# Create custom views of managed objects
You can customize the way Visual Studio displays data types in debugger variable windows.  
  
## Attributes  
 In C# and Visual Basic, you can add expansions for custom data using <xref:System.Diagnostics.DebuggerTypeProxyAttribute>, <xref:System.Diagnostics.DebuggerDisplayAttribute>, and <xref:System.Diagnostics.DebuggerBrowsableAttribute>.  
  
 In [!INCLUDE[dnprdnlong](../code-quality/includes/dnprdnlong_md.md)] code, Visual Basic does not support the DebuggerBrowsable attribute. This limitation is removed in more recent versions of the .NET Framework.  
  
## Visualizers  
 You can write a visualizer to display any managed data type. For more information, see [How to: Write a Visualizer](../debugger/how-to-write-a-visualizer.md).  
  
## Native Code  
 For native code, you can add custom data type expansions to the file autoexp.dat, which is located in the Program Files\Microsoft Visual Studio 11.0\Common7\Packages\Debugger directory. Instructions on how to write `autoexp` rules are located in the file itself.  
  
> [!CAUTION]
>  The structure of this file and the syntax of autoexp rules might change from one release of Visual Studio to the next.  
  
 Native type views can also be customized by writing an expression evaluator add-in. For more information, see [EEAddIn Sample: Debugging Expression Evaluator Add-In](http://msdn.microsoft.com/en-us/d4f6b068-c812-45bc-9ec0-7e0363c4bb9e).  
  
## See Also  
 [Using DebuggerTypeProxy Attribute](../debugger/using-debuggertypeproxy-attribute.md)   
 [Using the DebuggerDisplay Attribute](../debugger/using-the-debuggerdisplay-attribute.md)   
 [Watch and QuickWatch Windows](../debugger/watch-and-quickwatch-windows.md)   
 [Enhancing Debugging with the Debugger Display Attributes](/dotnet/framework/debug-trace-profile/enhancing-debugging-with-the-debugger-display-attributes)