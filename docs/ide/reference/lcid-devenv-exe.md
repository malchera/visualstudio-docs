---
title: -LCID (devenv.exe)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
  - "language default"
  - "locale IDs, setting for IDE"
  - "Devenv, /LCID switch"
  - "locale IDs"
  - "/l Devenv switch"
  - "LCID devenv switch"
  - "/lcid Devenv switch"
ms.assetid: 3a3f4e70-ea66-4351-9d62-acb1dec30e8e
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# /LCID (devenv.exe)
Sets the default language used for text, currency, and other values within the integrated development environment (IDE).

## Syntax

```cmd
devenv {/LCID|/l} LocaleID
```

## Arguments
 `LocaleID`
 Required. The LCID (locale ID) of the language you specify.

## Remarks
 Loads the IDE and sets the default natural language for the environment. This change is persisted between sessions and reflected on the **International Settings** pane of the **Environment** options in the **Options** dialog box in the IDE.

 If the specified language is not available on the user's system, the /LCID switch is ignored.

 The following table lists the LCIDs of the languages supported by [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)].

|Language|LCID|
|--------------|----------|
|Chinese (Simplified)|2052|
|Chinese (Traditional)|1028|
|English|1033|
|French|1036|
|German|1031|
|Italian|1040|
|Japanese|1041|
|Korean|1042|
|Spanish|3082|

## Example
 This example loads the IDE with English resources strings.

```cmd
devenv /LCID 1033
```

## See Also

- [Devenv Command Line Switches](../../ide/reference/devenv-command-line-switches.md)
- [International Settings, Environment, Options Dialog Box](../../ide/reference/international-settings-environment-options-dialog-box.md)
- [Customizing window layouts](../../ide/customizing-window-layouts-in-visual-studio.md)