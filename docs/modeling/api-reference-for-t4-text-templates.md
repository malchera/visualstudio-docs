---
title: API Reference for T4 Text Templates
ms.date: 11/04/2016
ms.topic: reference
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
ms.prod: visual-studio-dev15
ms.technology: vs-ide-modeling
---
# API Reference for T4 Text Templates

The Text Templating API lets you invoke and customize the transformation of [text templates](../modeling/code-generation-and-t4-text-templates.md).

## Namespaces

|Namespace|Purpose|
|---------------|-------------|
|<xref:Microsoft.VisualStudio.TextTemplating>|Contains classes for the text template transformation functionality. The text template transformation engine is integrated into Visual Studio, and transforms text template files into generated text output files.|
|<xref:Microsoft.VisualStudio.TextTemplating.Modeling>|Provides text transformation facilities related to UML models and domain-specific languages, such as access to [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] ModelBus.|
|<xref:Microsoft.VisualStudio.TextTemplating.VSHost>|Provides access to the text templating service in [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)].|