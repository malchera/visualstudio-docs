---
title: "KeyBindings Element | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.technology: 
  - "vs-ide-sdk"
ms.topic: "conceptual"
f1_keywords: 
  - "KeyBindings"
helpviewer_keywords: 
  - "VSCT XML schema elements, KeyBindings"
  - "KeyBindings element (VSCT XML schema)"
ms.assetid: 26a15d5c-ddea-4977-af7f-d795ff09c7ad
author: "gregvanl"
ms.author: "gregvanl"
manager: douge
ms.workload: 
  - "vssdk"
---
# KeyBindings Element
The KeyBindings element groups KeyBinding elements and other KeyBindings groupings.  
  
## Syntax  
  
```  
<KeyBindings>  
  <KeyBinding>... </KeyBinding>  
  <KeyBinding>... </KeyBinding>  
</KeyBindings>  
```  
  
## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  
  
### Attributes  
  
|Attribute|Description|  
|---------------|-----------------|  
|Condition|Optional. See [Conditional Attributes](../extensibility/vsct-xml-schema-conditional-attributes.md).|  
  
### Child Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[KeyBinding Element](../extensibility/keybinding-element.md)|Specifies keyboard shortcuts for the commands.|  
|[KeyBindings](../extensibility/keybindings-element.md)|Groups KeyBinding elements and other KeyBindings groupings.|  
  
### Parent Elements  
  
|Element|Description|  
|-------------|-----------------|  
|[CommandTable Element](../extensibility/commandtable-element.md)|Defines all the elements that represent commands.|  
  
## Example  
  
```  
<KeyBindings>  
  <KeyBinding guid="guidWidgetPackage" id="cmdidUpdateWidget"   
    editor="guidWidgetEditor" key1="VK_F5"/>  
  <KeyBinding guid="guidWidgetPackage" id="cmdidRunWidget"   
    editor="guidWidgetEditor" key1="VK_F5" mod1="Control"/>  
</KeyBindings>  
```  
  
## See Also  
 [KeyBinding Element](../extensibility/keybinding-element.md)   
 [Visual Studio Command Table (.Vsct) Files](../extensibility/internals/visual-studio-command-table-dot-vsct-files.md)