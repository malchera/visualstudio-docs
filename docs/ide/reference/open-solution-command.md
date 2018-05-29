---
title: Open Solution Command
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-general
ms.topic: reference
f1_keywords:
  - "file.opensolution"
helpviewer_keywords:
  - "Open Solution command"
  - "File.OpenSolution command"
ms.assetid: 61de76c8-69d7-4cdb-b605-e132f45d05d9
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# Open Solution Command
Opens an existing solution, closing any other open solutions.

## Syntax

```cmd
File.OpenSolution filename
```

## Arguments
 `Filename`

 Required. The full path and file name of the solution to open.

 The syntax for the `filename` argument requires that paths containing spaces use quotation marks.

## Remarks
 Auto completion tries to locate the correct path and file name as you type.

## Example
 This example opens the solution, Test1.sln.

```cmd
>File.OpenSolution "c:\MySolutions\Test1\Test1.sln"
```

## See Also

- [Visual Studio Commands](../../ide/reference/visual-studio-commands.md)
- [Command Window](../../ide/reference/command-window.md)
- [Find/Command Box](../../ide/find-command-box.md)
- [Visual Studio Command Aliases](../../ide/reference/visual-studio-command-aliases.md)