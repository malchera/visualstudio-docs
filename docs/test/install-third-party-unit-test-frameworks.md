---
title: "Install third-party unit test frameworks in Visual Studio"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.technology: vs-ide-test
ms.topic: conceptual
ms.author: gewarren
manager: douge
ms.workload: 
  - "multiple"
author: gewarren
---
# Install third-party unit test frameworks

Visual Studio Test Explorer can run any unit test framework that has developed an adapter interface for the Explorer. The install program of the framework installs the binaries and adds Visual Studio project templates for the languages it supports. When you create a project with the template, the framework is registered with Test Explorer. A Visual Studio solution can contain unit test projects that use different frameworks and that are targeted at different languages. Test Explorer runs them all.

## Acquiring third-party frameworks

You can download and install many third-party unit test frameworks by using the Visual Studio Extension Manager, or from the Visual Studio Marketplace. Frameworks can also be downloaded from other sites such as the website of the framework.

### Installing from Visual Studio

1. Choose **Tools** on the standard menu, and then choose **Extensions and Updates**.

2. Expand **Online** > **Visual Studio Marketplace** > **Tools**. Choose **Testing**.

3. Browse the list to find the framework.

4. Select the framework and choose **Download**.

For more information see [Finding and Using Visual Studio Extensions](../ide/finding-and-using-visual-studio-extensions.md).

### Installing from the web

If you know the framework you are interested in:

1. Open [Visual Studio Marketplace](https://marketplace.visualstudio.com/vs).

2. Type the name of the framework in the **Find** box.

3. Choose the framework in the results list to navigate to the Visual Studio Marketplace page for the tool.

To browse a list of frameworks along with other testing tools:

1. Open [Visual Studio Marketplace](https://marketplace.visualstudio.com/vs).

2. In **Filter by category / collection**, choose **See all**.

3. In the **Category** list (labeled as **Showing**), expand the **Tools** node and then choose **Testing**.

4. Choose a framework in the results list to navigate to a Visual Studio Marketplace page for the tool.

## See also

- [Unit Test Your Code](../test/unit-test-your-code.md)
