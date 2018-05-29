---
title: "Create web templates for Visual Studio"
ms.date: 01/02/2018
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: conceptual
helpviewer_keywords:
  - "Visual Studio templates, Web"
  - "templates [Visual Studio], Web"
  - "Web templates [Visual Studio]"
  - "project templates [Visual Studio], Web"
author: gewarren
ms.author: gewarren
manager: douge
---
# How to: Manually create web templates

Creating a web template is different than creating other kinds of templates. Because web project templates appear in the **Add New Web Site** dialog box, and web project items are categorized by programming language, the *vstemplate* file must specify the template as a web template and identify the programming language.

> [!NOTE]
> Web templates must contain an empty *.webproj* file, and it must be referenced in the *vstemplate* file in the `File` attribute of the `Project` element. Although Web projects do not require a *.proj* project file, it's necessary to create this stub file for the web template to function correctly.

## To manually create a web template

1. Create a web project.

1. Modify or delete the files in the project, or add new files to the project.

1. Create an XML file and save it with a *vstemplate* file name extension, in the same directory as your project. Do not add it to the project in Visual Studio.

1. Edit the *vstemplate* XML file to provide project template metadata. For more information, see the [example that follows](#example).

1. Locate the `ProjectType` element in the *vstemplate* file, and set the text value to `Web`.

1. Following the `ProjectType` element, add a `ProjectSubType` element and set the text value to the programming language of the template. The programming language can be one of the following values:

    - CSharp
    - VisualBasic

    For example:

    ```xml
    <TemplateData>
        ...
        <ProjectType>Web</ProjectType>
        <ProjectSubType>CSharp</ProjectSubType>
        ...
    </TemplateData>
    ```

1. Select the files in your template (this includes the *vstemplate* file), right-click the selection, and choose **Send to** > **Compressed (zipped) folder**. The files are compressed into a *.zip* file.

1. Put the *.zip* template file in the Visual Studio project template directory. By default, this directory is *%USERPROFILE%\Documents\Visual Studio \<Version\>\ProjectTemplates*.

## Example

The following example shows a basic *vstemplate* file for a web project template:

```xml
<VSTemplate Version="2.0.0" Type="Project"
    xmlns="http://schemas.microsoft.com/developer/vstemplate/2005">>
    <TemplateData>
        <Name>MyWebProjecStarterKit</Name>
        <Description>A simple Web template</Description>
        <Icon>icon.ico</Icon>
        <ProjectType>Web</ProjectType>
        <ProjectSubType>CSharp</ProjectSubType>
        <DefaultName>WebSite</DefaultName>
    </TemplateData>
    <TemplateContent>
        <Project File="WebApplication.webproj">
            <ProjectItem>icon.ico</ProjectItem>
            <ProjectItem OpenInEditor="true">Default.aspx</ProjectItem>
            <ProjectItem>Default.aspx.cs</ProjectItem>
        </Project>
    </TemplateContent>
</VSTemplate>
```

## See also

- [Create project and item templates](../ide/creating-project-and-item-templates.md)
- [Visual Studio template schema reference (extensibility)](../extensibility/visual-studio-template-schema-reference.md)