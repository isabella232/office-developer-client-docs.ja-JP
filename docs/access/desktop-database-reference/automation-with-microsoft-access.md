---
title: Microsoft Access によるオートメーション
TOCTitle: Automation with Microsoft Access
description: Microsoft Access は、オートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 9635cdb2a06f610f42e4aa9fc9f998719aebb986
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296963"
---
# <a name="automation-with-microsoft-access"></a><span data-ttu-id="32097-103">Microsoft Access によるオートメーション</span><span class="sxs-lookup"><span data-stu-id="32097-103">Automation with Microsoft Access</span></span>

<span data-ttu-id="32097-104">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="32097-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32097-p101">Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="32097-p101">Microsoft Access is a COM component that supports Automation, formerly called OLE Automation. Microsoft Access supports Automation in two ways. From Microsoft Access, you can work with objects supplied by another component. Microsoft Access also supplies its objects to other COM components.</span></span>

<span data-ttu-id="32097-p102">**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="32097-p102">You can use the **New** keyword or the **CreateObject** method to create a new instance of a component. You can use the **GetObject** method to assign a variable to an existing instance of a component.</span></span>

<span data-ttu-id="32097-p103">Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="32097-p103">In Microsoft Access, you can set a reference to a component's type library to improve performance when you work with that component through Automation. Microsoft Access also includes the Object Browser, a tool that enables you to view objects in another component's type library, as well as their methods and properties.</span></span>

<span data-ttu-id="32097-113">Microsoft Access タイプ ライブラリでは、Microsoft Access オブジェクトに関する情報が他のコンポーネントに提供されます。</span><span class="sxs-lookup"><span data-stu-id="32097-113">The Microsoft Access type library provides information about Microsoft Access objects to other components.</span></span> <span data-ttu-id="32097-114">コンポーネントから Microsoft Access タイプ ライブラリへの[参照を設定](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries)すると、オブジェクト ブラウザーでタイプ ライブラリ内のオブジェクトを表示できます。</span><span class="sxs-lookup"><span data-stu-id="32097-114">You can [set a reference](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries)
 to the Microsoft Access type library from a component and view its objects in the Object Browser.</span></span>

<span data-ttu-id="32097-p105">オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。</span><span class="sxs-lookup"><span data-stu-id="32097-p105">To work with Microsoft Access objects through Automation, you must create an instance of the Microsoft Access **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** object. For example, suppose you want to display data from Microsoft Excel in a Microsoft Access form or report. To launch Microsoft Access from Microsoft Excel, you can use the **New** keyword to create an instance of the Microsoft Access **Application** object. You can also use the **CreateObject** method to create a new instance of the Microsoft Access **Application** object, or you can use the **GetObject** method to point an object variable to an existing instance of Microsoft Access. Check your component's documentation to determine which syntax it supports.</span></span>

<span data-ttu-id="32097-120">Microsoft Access のインスタンスを開始した後、Microsoft Access のオブジェクトを操作するには、**[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** または **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** メソッドを使用して Microsoft Access ウィンドウにデータベースを開くか、あるいは、**[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** または **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** メソッドを使用して Microsoft Access ウィンドウにプロジェクト (.adp) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="32097-120">Once you've launched an instance of Microsoft Access, if you want to control any Microsoft Access objects, you must open a database or project (.adp) in the Microsoft Access window by using either the **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** or the **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** method for a database or by using the **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** or the **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** method for a project.</span></span>

<span data-ttu-id="32097-121">Microsoft DAO が提供する Data Access Objects を使用する手段としてのみ Microsoft Access を開いている場合は、Microsoft Access ウィンドウでデータベースを開く必要はありません。</span><span class="sxs-lookup"><span data-stu-id="32097-121">If you've opened Microsoft Access only as a means of using the Data Access Objects provided by Microsoft DAO, then you don't need to open a database in the Microsoft Access window.</span></span> <span data-ttu-id="32097-122">オートメーションの操作中に Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリのオブジェクトにアクセスするには、Microsoft Access **アプリケーション** オブジェクトの **[ DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="32097-122">You can use the **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** property of the Microsoft Access **Application** object to access objects in the Microsoft Office 12.0 Access Database Engine Object Library object library during an Automation operation.</span></span>

