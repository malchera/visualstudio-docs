---
title: -DebugExe (devenv.exe)
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
helpviewer_keywords:
  - "Devenv, /DebugExe switch"
  - "DebugExe switch"
  - "/DebugExe [devenv.exe]"
ms.assetid: cd700006-1648-418f-924b-4b1e5c1412ab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# /DebugExe (devenv.exe)
Opens the specified executable file to be debugged.

## Syntax

```cmd
Devenv /debugexe ExecutableFile
```

## Arguments
 `ExecutableFile`

 Required. The path and file name of an .exe file.

 If the .exe file is not found or does not exist, no warning or error is displayed and [!INCLUDE[vsprvs](../../code-quality/includes/vsprvs_md.md)] starts normally.

## Remarks
 Any strings following the `ExecutableFile` parameter are passed to that file as arguments.

## Example
 The following example opens the file `MyApplication.exe` for debugging.

```cmd
Devenv.exe /debugexe MyApplication.exe
```

## See Also

- [Devenv Command Line Switches](../../ide/reference/devenv-command-line-switches.md)