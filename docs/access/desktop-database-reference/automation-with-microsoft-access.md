---
title: Access でのオートメーションのサポート
TOCTitle: Automation with Microsoft Access
description: Microsoft Access は、OLE オートメーションと呼ばれていたオートメーションをサポートする COM コンポーネントです。
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 5104ab19c5fab816040d7a5d56fa6f425658c245
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874252"
---
# <a name="automation-with-microsoft-access"></a><span data-ttu-id="e7367-103">Microsoft Access によるオートメーション</span><span class="sxs-lookup"><span data-stu-id="e7367-103">Automation with Microsoft Access</span></span>

<span data-ttu-id="e7367-104">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e7367-104">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e7367-p101">Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="e7367-p101">Microsoft Access is a COM component that supports Automation, formerly called OLE Automation. Microsoft Access supports Automation in two ways. From Microsoft Access, you can work with objects supplied by another component. Microsoft Access also supplies its objects to other COM components.</span></span>

<span data-ttu-id="e7367-p102">**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="e7367-p102">You can use the **New** keyword or the **CreateObject** method to create a new instance of a component. You can use the **GetObject** method to assign a variable to an existing instance of a component.</span></span>

<span data-ttu-id="e7367-p103">Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="e7367-p103">In Microsoft Access, you can set a reference to a component's type library to improve performance when you work with that component through Automation. Microsoft Access also includes the Object Browser, a tool that enables you to view objects in another component's type library, as well as their methods and properties.</span></span>

<span data-ttu-id="e7367-113">Access のタイプ ライブラリには、Access オブジェクトに関する情報が格納されており、この情報はそのオブジェクトを使用する他のコンポーネントに渡されます。</span><span class="sxs-lookup"><span data-stu-id="e7367-113">The Microsoft Access type library provides information about Microsoft Access objects to other components.</span></span> <span data-ttu-id="e7367-114">Microsoft Access[の参照を設定](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries)することができます、コンポーネントからライブラリを入力し、オブジェクト ブラウザー内のオブジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="e7367-114">You can [set a reference](https://docs.microsoft.com/office/vba/access/Concepts/Settings/set-references-to-type-libraries) to the Microsoft Access type library from a component and view its objects in the Object Browser.</span></span>

<span data-ttu-id="e7367-p105">オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。</span><span class="sxs-lookup"><span data-stu-id="e7367-p105">To work with Microsoft Access objects through Automation, you must create an instance of the Microsoft Access **[Application](https://docs.microsoft.com/office/vba/api/Access.Application)** object. For example, suppose you want to display data from Microsoft Excel in a Microsoft Access form or report. To launch Microsoft Access from Microsoft Excel, you can use the **New** keyword to create an instance of the Microsoft Access **Application** object. You can also use the **CreateObject** method to create a new instance of the Microsoft Access **Application** object, or you can use the **GetObject** method to point an object variable to an existing instance of Microsoft Access. Check your component's documentation to determine which syntax it supports.</span></span>

<span data-ttu-id="e7367-120">後、Microsoft Access のインスタンスを起動したは、Microsoft Access オブジェクトを制御する場合、開く必要がありますデータベースまたはプロジェクト (.adp) Microsoft Access のウィンドウで、 **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** または NewCurrentDatabase の**[を使用して](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** メソッドのデータベースまたはプロジェクトの**[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** または**[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** メソッドを使用しています。</span><span class="sxs-lookup"><span data-stu-id="e7367-120">After you've launched an instance of Microsoft Access, if you want to control any Microsoft Access objects, you must open a database or project (.adp) in the Microsoft Access window by using either the **[OpenCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.OpenCurrentDatabase)** or the **[NewCurrentDatabase](https://docs.microsoft.com/office/vba/api/Access.Application.NewCurrentDatabase)** method for a database or by using the **[OpenAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.OpenAccessProject)** or the **[NewAccessProject](https://docs.microsoft.com/office/vba/api/Access.Application.NewAccessProject)** method for a project.</span></span>

<span data-ttu-id="e7367-121">Dao データ アクセス オブジェクトを使用するための手段として Microsoft Access を開いた場合、Access ウィンドウにデータベースを開く必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e7367-121">If you've opened Microsoft Access only as a means of using the Data Access Objects provided by Microsoft DAO, you don't need to open a database in the Microsoft Access window.</span></span> <span data-ttu-id="e7367-122">オートメーションの操作中に、Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリで、 **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** オブジェクトのプロパティ、Microsoft Access の**アプリケーション**オブジェクトにアクセスするを使用できます。</span><span class="sxs-lookup"><span data-stu-id="e7367-122">You can use the **[DBEngine](https://docs.microsoft.com/office/vba/api/Access.Application.DBEngine)** property of the Microsoft Access **Application** object to access objects in the Microsoft Office 12.0 Access Database Engine Object Library during an Automation operation.</span></span>

