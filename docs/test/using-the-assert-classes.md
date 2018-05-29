---
title: "Using the Assert Classes for unit testing in Visual Studio"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: reference
helpviewer_keywords: 
  - "Assert classes"
  - "Assert statements"
  - "unit tests, Assert statements"
  - "unit tests, Assert classes"
ms.author: gewarren
manager: douge
ms.workload: 
  - "multiple"
author: gewarren
---
# Use the Assert Classes

Use the Assert classes of the UnitTestingFramework namespace to verify specific functionality. A unit test method exercises the code of a method in your development code, but it reports the correctness of the code's behavior only if you include Assert statements.

## Kinds of Asserts

 The <xref:Microsoft.VisualStudio.TestTools.UnitTesting> namespace provides several kinds of Assert classes:

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.Assert>

 In your test method, you can call any number of methods of the Assert class, such as Assert.AreEqual(). The Assert class has many methods to choose from, and many of those methods have several overloads.

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.CollectionAssert>

 Use the CollectionAssert class to compare collections of objects, and to verify the state of one or more collections.

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.StringAssert>

 Use the StringAssert class to compare strings. This class contains a variety of useful methods such as StringAssert.Contains, StringAssert.Matches, and StringAssert.StartsWith.

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertFailedException>

 The AssertFailedException exception is thrown whenever a test fails. A test fails if it times out, throws an unexpected exception, or contains an Assert statement that produces a Failed result.

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.AssertInconclusiveException>

 The AssertInconclusiveException is thrown whenever a test produces a result of Inconclusive. Typically, you add an Assert.Inconclusive statement to a test that you are still working on to indicate it is not yet ready to be run.

> [!NOTE]
> An alternative strategy is to mark a test that is not ready to run with the Ignore attribute. However, this has the disadvantage that you cannot easily generate a report on the number of tests you have left to implement.

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.UnitTestAssertException>

 If you write a new Assert exception class, having that class inherit from the base class UnitTestAssertException makes it easier to identify the exception as an assertion failure instead of an unexpected exception thrown from your test or production code.

 <xref:Microsoft.VisualStudio.TestTools.UnitTesting.ExpectedExceptionAttribute>

 Decorate a test method with the ExpectedExceptionAttribute attribute when you want the test method to verify that an exception you expect to be thrown by a method in your development code is indeed being thrown in that method.

## See also

- <xref:Microsoft.VisualStudio.TestTools.UnitTesting>
- [Unit test your code](../test/unit-test-your-code.md)
