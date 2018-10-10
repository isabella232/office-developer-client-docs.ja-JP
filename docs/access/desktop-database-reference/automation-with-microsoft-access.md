---
title: Access でのオートメーションのサポート
TOCTitle: Automation with Microsoft Access
ms:assetid: 39fde349-3ba3-7c7a-3c92-316641dc8712
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192643(v=office.15)
ms:contentKeyID: 48544258
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13783
f1_categories:
- Office.Version=v15
ms.openlocfilehash: bd0e230d2b4c31d497e913e8e1ccf4d2172402e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478224"
---
# <a name="automation-with-microsoft-access"></a><span data-ttu-id="f681d-102">Access でのオートメーションのサポート</span><span class="sxs-lookup"><span data-stu-id="f681d-102">Automation with Microsoft Access</span></span>


<span data-ttu-id="f681d-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="f681d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="f681d-p101">Access はオートメーション (以前の OLE オートメーション) をサポートする COM コンポーネントです。このオートメーションのサポートには 2 つの方法があります。つまり、他の COM コンポーネントのオブジェクトを Access で使用することもできれば、Access のオブジェクトを他の COM コンポーネントで使用することもできます。</span><span class="sxs-lookup"><span data-stu-id="f681d-p101">Microsoft Access is a COM component that supports Automation, formerly called OLE Automation. Microsoft Access supports Automation in two ways. From Microsoft Access, you can work with objects supplied by another component. Microsoft Access also supplies its objects to other COM components.</span></span>

<span data-ttu-id="f681d-p102">**New** キーワードまたは **CreateObject** メソッドを使用すると、コンポーネントの新規インスタンスを作成できます。 **GetObject** メソッドを使用すると、コンポーネントの既存のインスタンスに変数を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f681d-p102">You can use the **New** keyword or the **CreateObject** method to create a new instance of a component. You can use the **GetObject** method to assign a variable to an existing instance of a component.</span></span>

<span data-ttu-id="f681d-p103">Access では、コンポーネントのタイプ ライブラリへの参照を設定することで、オートメーションを通じてそのコンポーネントを処理する際のパフォーマンスを向上させることができます。また、Access のオブジェクト ブラウザーでは、他のコンポーネントのタイプ ライブラリのオブジェクトやメソッド、プロパティを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f681d-p103">In Microsoft Access, you can set a reference to a component's type library to improve performance when you work with that component through Automation. Microsoft Access also includes the Object Browser, a tool that enables you to view objects in another component's type library, as well as their methods and properties.</span></span>

<span data-ttu-id="f681d-112">Access のタイプ ライブラリには、Access オブジェクトに関する情報が格納されており、この情報はそのオブジェクトを使用する他のコンポーネントに渡されます。</span><span class="sxs-lookup"><span data-stu-id="f681d-112">The Microsoft Access type library provides information about Microsoft Access objects to other components.</span></span> <span data-ttu-id="f681d-113">Microsoft Access[の参照を設定](https://msdn.microsoft.com/library/ff194944\(v=office.15\))することができます、コンポーネントからライブラリを入力し、オブジェクト ブラウザー内のオブジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="f681d-113">You can [set a reference](https://msdn.microsoft.com/library/ff194944\(v=office.15\)) to the Microsoft Access type library from a component and view its objects in the Object Browser.</span></span>

<span data-ttu-id="f681d-p105">オートメーションを通じて Microsoft Access オブジェクトを処理するには、Microsoft Access の **[Application](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** オブジェクトのインスタンスを作成する必要があります。たとえば、Microsoft Access のフォームまたはレポートに Microsoft Excel のデータを表示するとします。このような場合に Microsoft Excel から Microsoft Access を起動するには、キーワード **New** を使って Microsoft Access の **Application** オブジェクトのインスタンスを作成するという方法があります。他にも、 **CreateObject** メソッドを使って Microsoft Access の **Application** オブジェクトの新規インスタンスを作成する方法や、 **GetObject** メソッドを使って Microsoft Access の既存のインスタンスへのオブジェクト変数を示す方法があります。これらのうち、コンポーネントがどの方法をサポートしているかは、そのコンポーネントのマニュアルで確認してください。</span><span class="sxs-lookup"><span data-stu-id="f681d-p105">To work with Microsoft Access objects through Automation, you must create an instance of the Microsoft Access **[Application](https://msdn.microsoft.com/library/ff821758\(v=office.15\))** object. For example, suppose you want to display data from Microsoft Excel in a Microsoft Access form or report. To launch Microsoft Access from Microsoft Excel, you can use the **New** keyword to create an instance of the Microsoft Access **Application** object. You can also use the **CreateObject** method to create a new instance of the Microsoft Access **Application** object, or you can use the **GetObject** method to point an object variable to an existing instance of Microsoft Access. Check your component's documentation to determine which syntax it supports.</span></span>

<span data-ttu-id="f681d-119">Microsoft Access のインスタンスを開始した後、Microsoft Access のオブジェクトを操作するには、 **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))** または **[NewCurrentDatabase](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** メソッドを使って Microsoft Access ウィンドウにデータベースを開くか、あるいは、 **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))** または **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** メソッドを使って Microsoft Access ウィンドウにプロジェクト (.adp) を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="f681d-119">Once you've launched an instance of Microsoft Access, if you want to control any Microsoft Access objects, you must open a database or project (.adp) in the Microsoft Access window by using either the **[OpenCurrentDatabase](https://msdn.microsoft.com/library/ff837226\(v=office.15\))** or the **[NewCurrentDatabase](https://msdn.microsoft.com/library/ff195271\(v=office.15\))** method for a database or by using the **[OpenAccessProject](https://msdn.microsoft.com/library/ff837249\(v=office.15\))** or the **[NewAccessProject](https://msdn.microsoft.com/library/ff835758\(v=office.15\))** method for a project.</span></span>

<span data-ttu-id="f681d-120">Dao データ アクセス オブジェクトを使用するための手段として Microsoft Access を開いた場合は、Microsoft Access のウィンドウでデータベースを開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="f681d-120">If you've opened Microsoft Access only as a means of using the Data Access Objects provided by Microsoft DAO, then you don't need to open a database in the Microsoft Access window.</span></span> <span data-ttu-id="f681d-121">オートメーションの操作中に、Microsoft Office 12.0 Access データベース エンジン オブジェクト ライブラリのオブジェクト ライブラリで、 **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** オブジェクトのプロパティ、Microsoft Access の**アプリケーション**オブジェクトにアクセスするを使用できます。</span><span class="sxs-lookup"><span data-stu-id="f681d-121">You can use the **[DBEngine](https://msdn.microsoft.com/library/ff821724\(v=office.15\))** property of the Microsoft Access **Application** object to access objects in the Microsoft Office 12.0 Access Database Engine Object Library object library during an Automation operation.</span></span>

