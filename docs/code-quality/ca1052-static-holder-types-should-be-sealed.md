---
title: "CA1052: Static holder types should be sealed"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-code-analysis
ms.topic: reference
f1_keywords:
  - "StaticHolderTypesShouldBeSealed"
  - "CA1052"
helpviewer_keywords:
  - "CA1052"
  - "StaticHolderTypesShouldBeSealed"
ms.assetid: 51a3165d-781e-4a55-aa0d-ea25fee7d4f2
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# CA1052: Static holder types should be sealed
|||
|-|-|
|TypeName|StaticHolderTypesShouldBeSealed|
|CheckId|CA1052|
|Category|Microsoft.Design|
|Breaking Change|Breaking|

## Cause
 A public or protected type contains only static members and is not declared with the [sealed](/dotnet/csharp/language-reference/keywords/sealed) ([NotInheritable](/dotnet/visual-basic/language-reference/modifiers/notinheritable)) modifier.

## Rule Description
 This rule assumes that a type that contains only static members is not designed to be inherited, because the type does not provide any functionality that can be overridden in a derived type. A type that is not meant to be inherited should be marked with the `sealed` modifier to prohibit its use as a base type.

## How to Fix Violations
 To fix a violation of this rule, mark the type as `sealed`. If you are targeting [!INCLUDE[dnprdnshort](../code-quality/includes/dnprdnshort_md.md)] 2.0 or later, a better approach is to mark the type as `static`. In this manner, you avoid having to declare a private constructor to prevent the class from being created.

## When to Suppress Warnings
 Suppress a warning from this rule only if the type is designed to be inherited. The absence of the `sealed` modifier suggests that the type is useful as a base type.

## Example of a Violation

### Description
 The following example shows a type that violates the rule.

### Code
 [!code-csharp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_1.cs)]
 [!code-vb[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/VisualBasic/ca1052-static-holder-types-should-be-sealed_1.vb)]
 [!code-cpp[FxCop.Design.StaticMembers#1](../code-quality/codesnippet/CPP/ca1052-static-holder-types-should-be-sealed_1.cpp)]

## Fix with the Static Modifier

### Description
 The following example shows how to fix a violation of this rule by marking the type with the `static` modifier.

### Code
 [!code-csharp[FxCop.Design.StaticMembersFixed#1](../code-quality/codesnippet/CSharp/ca1052-static-holder-types-should-be-sealed_2.cs)]

## Related Rules
 [CA1053: Static holder types should not have constructors](../code-quality/ca1053-static-holder-types-should-not-have-constructors.md)
