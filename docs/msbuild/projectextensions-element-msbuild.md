---
title: "ProjectExtensions Element (MSBuild) | Microsoft Docs"
ms.custom: ""
ms.date: "03/13/2017"
ms.technology: msbuild
ms.topic: "reference"
f1_keywords: 
  - "http://schemas.microsoft.com/developer/msbuild/2003#ProjectExtensions"
dev_langs: 
  - "VB"
  - "CSharp"
  - "C++"
  - "jsharp"
helpviewer_keywords: 
  - "<ProjectExtensions> element [MSBuild]"
  - "ProjectExtensions element [MSBuild]"
ms.assetid: f95f312f-ff92-41eb-9469-ad99e236a307
author: mikejo5000
ms.author: mikejo
manager: douge
ms.workload: 
  - "multiple"
---
# ProjectExtensions Element (MSBuild)
Allows [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] project files to contain non-[!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] information. Anything inside of a `ProjectExtensions` element will be ignored by [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)].  

 \<Project>  
 \<ProjectExtensions>  

## Syntax  

```  
<ProjectExtensions>  
    Non-MSBuild information to include in file.  
</ProjectExtensions>  
```  

## Attributes and Elements  
 The following sections describe attributes, child elements, and parent elements.  

### Attributes  
 None  

### Child Elements  
 None  

### Parent Elements  

|Element|Description|  
|-------------|-----------------|  
|[Project](../msbuild/project-element-msbuild.md)|Required root element of an [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] project file.|  

## Remarks  
 Only one `ProjectExtensions` element may be used in an [!INCLUDE[vstecmsbuild](../extensibility/internals/includes/vstecmsbuild_md.md)] project.  

## Example  
 The following code example shows information from the integrated development environment being stored in a `ProjectExtensions` element.  

```xml  
<ProjectExtensions>  
    <VSIDE>  
        <External>  
            <!--  
            Raw XML passed to the IDE by an external source  
            -->  
        </External>  
    </VSIDE>  
</ProjectExtensions>  
```  

## See Also  
 [Project File Schema Reference](../msbuild/msbuild-project-file-schema-reference.md)  
 [MSBuild](../msbuild/msbuild.md)
