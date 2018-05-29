---
title: "ItemDefinitionGroup Element (MSBuild) | Microsoft Docs"
ms.custom: ""
ms.date: "03/13/2017"
ms.technology: msbuild
ms.topic: "reference"
f1_keywords: 
  - "http://schemas.microsoft.com/developer/msbuild/2003#ItemDefinitionGroup"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "ItemDefinitionGroup Element [MSBuild]"
  - "<ItemDefinitionGroup> Element [MSBuild]"
ms.assetid: 4e9fb04b-5148-4ae5-a394-42861dd62371
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload: 
  - "multiple"
---
# ItemDefinitionGroup Element (MSBuild)
The `ItemDefinitionGroup` element lets you define a set of Item Definitions, which are metadata values that are applied to all items in the project, by default. ItemDefinitionGroup supersedes the need to use the [CreateItem Task](../msbuild/createitem-task.md) and the [CreateProperty Task](../msbuild/createproperty-task.md). For more information, see [Item Definitions](../msbuild/item-definitions.md).  

 \<Project>  
 \<ItemDefinitionGroup>  

## Syntax  

```  
<ItemDefinitionGroup Condition="'String A' == 'String B'">  
    <Item1>... </Item1>  
    <Item2>... </Item2>  
</ItemDefinitionGroup>  
```  

## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  

### Attributes  

|Attribute|Description|  
|---------------|-----------------|  
|`Condition`|Optional attribute. Condition to be evaluated. For more information, see [Conditions](../msbuild/msbuild-conditions.md).|  

### Child Elements  

|Element|Description|  
|-------------|-----------------|  
|[Item](../msbuild/item-element-msbuild.md)|Defines the inputs for the build process. There may be zero or more `Item` elements in an `ItemDefinitionGroup`.|  

### Parent Elements  

|Element|Description|  
|-------------|-----------------|  
|[Project](../msbuild/project-element-msbuild.md)|Required root element of an [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] project file.|  

## Example  
 The following code example defines two metadata items, m and n, in an ItemDefinitionGroup. In this example, the default metadata "m" is applied to Item "i" because metadata "m" is not explicitly defined by Item "i". However, default metadata "n" is not applied to Item "i" because metadata "n" is already defined by Item "i".  

```xml  
<Project xmlns="http://schemas.microsoft.com/developer/msbuild/2003">  
    <ItemDefinitionGroup>  
        <i>  
            <m>m1</m>  
            <n>n1</n>  
        </i>        
    </ItemDefinitionGroup>  
    <ItemGroup>  
        <i Include="a">  
            <o>o1</o>  
            <n>n2</n>  
        </i>  
    </ItemGroup>  
    ...  
</Project>  
```  

## See Also  
 [Project File Schema Reference](../msbuild/msbuild-project-file-schema-reference.md)   
 [Items](../msbuild/msbuild-items.md)
