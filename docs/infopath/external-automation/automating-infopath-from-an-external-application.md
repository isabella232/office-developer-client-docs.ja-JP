---
title: InfoPath を自動化する外部のアプリケーションから
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath では、アプリケーションのオブジェクトおよび XDocuments コレクションのメソッドを使用して COM オブジェクトとスクリプトを使用して記述されたコードからのアプリケーションの自動化を提供します。
ms.openlocfilehash: 0e3fcc50ec11f5fc8791d37144767bf0398ccda7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799003"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="d9836-103">InfoPath を自動化する外部のアプリケーションから</span><span class="sxs-lookup"><span data-stu-id="d9836-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="d9836-104">Microsoft InfoPath では、**アプリケーション**のオブジェクトおよび**XDocuments**コレクションのメソッドを使用して COM オブジェクトとスクリプトを使用して記述されたコードからのアプリケーションの自動化を提供します。</span><span class="sxs-lookup"><span data-stu-id="d9836-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="d9836-105">アプリケーションおよび XDocument オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="d9836-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="d9836-106">**Application** オブジェクトには、オートメーションに使用される次のメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9836-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="d9836-107">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="d9836-107">**Method**</span></span>|<span data-ttu-id="d9836-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9836-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9836-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="d9836-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="d9836-110">調べ、キャッシュにし、必要に応じて、フォーム テンプレートの発行された場所から更新します。</span><span class="sxs-lookup"><span data-stu-id="d9836-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="d9836-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="d9836-111">**Quit**</span></span> <br/> |<span data-ttu-id="d9836-112">Microsoft Office InfoPath アプリケーションを終了します。</span><span class="sxs-lookup"><span data-stu-id="d9836-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="d9836-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="d9836-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="d9836-114">指定された Microsoft Office InfoPath フォーム テンプレートをインストールします。</span><span class="sxs-lookup"><span data-stu-id="d9836-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="d9836-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="d9836-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="d9836-116">指定された Microsoft Office InfoPath フォーム テンプレートをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="d9836-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="d9836-117">**XDocuments** コレクションには、外部の自動化に使用できる以下のメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="d9836-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="d9836-118">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="d9836-118">**Method**</span></span>|<span data-ttu-id="d9836-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="d9836-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d9836-120">**Close** メソッド</span><span class="sxs-lookup"><span data-stu-id="d9836-120">**Close** method</span></span>  <br/> |<span data-ttu-id="d9836-121">指定された Microsoft Office InfoPath フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="d9836-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="d9836-122">**New** メソッド</span><span class="sxs-lookup"><span data-stu-id="d9836-122">**New** method</span></span>  <br/> |<span data-ttu-id="d9836-123">新しい Microsoft Office InfoPath フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9836-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="d9836-124">**NewFromSolution** メソッド</span><span class="sxs-lookup"><span data-stu-id="d9836-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="d9836-125">指定したフォーム テンプレートに基づいて、新しい Microsoft Office InfoPath フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9836-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="d9836-126">**NewFromSolutionWithData** メソッド</span><span class="sxs-lookup"><span data-stu-id="d9836-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="d9836-127">指定した XML データとフォーム テンプレートを使用して、新しい Microsoft Office InfoPath フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="d9836-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="d9836-128">**Open** メソッド</span><span class="sxs-lookup"><span data-stu-id="d9836-128">**Open** method</span></span>  <br/> |<span data-ttu-id="d9836-129">指定された Microsoft Office InfoPath フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="d9836-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="d9836-p101">外部アプリケーションから **Application** オブジェクトを使用するには、**CreateObject** 関数と InfoPath アプリケーションの ProgID ("InfoPath.Application") を使用して、InfoPath アプリケーションを表すオブジェクト変数を作成します。次に、**XDocuments** プロパティを使用して **XDocuments** コレクションにアクセスし、メソッドを使用して InfoPath フォームを開くか作成します。次の例では、Microsoft Visual Basic 6.0 または Visual Basic for Applications (VBA) プログラミング言語を使用する **Application** オブジェクトへの参照の作成を示します。</span><span class="sxs-lookup"><span data-stu-id="d9836-p101">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application. You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form. The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="d9836-p102">**CreateObject** 関数は、遅延バインディングを使用してオブジェクト変数を作成するため、Visual Basic Editor ではステートメントの自動補完を利用できません。正しい呼び出し構文の詳細については、上記の表のリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="d9836-p102">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor. Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

