---
title: 外部アプリケーションからの InfoPath の自動化
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d2248d9-ab20-bcaa-d75b-62876c5e95eb
description: Microsoft InfoPath では、application オブジェクトと XDocuments コレクションのメソッドを使用して、COM およびスクリプトを使用して記述されたコードからアプリケーションを自動化できます。
ms.openlocfilehash: 7eccbca34b93aff7909de92eebc04d012d4dd97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412668"
---
# <a name="automating-infopath-from-an-external-application"></a><span data-ttu-id="52750-103">外部アプリケーションからの InfoPath の自動化</span><span class="sxs-lookup"><span data-stu-id="52750-103">Automating InfoPath from an external application</span></span>

<span data-ttu-id="52750-104">Microsoft InfoPath では、 **application**オブジェクトと**XDocuments**コレクションのメソッドを使用して、COM およびスクリプトを使用して記述されたコードからアプリケーションを自動化できます。</span><span class="sxs-lookup"><span data-stu-id="52750-104">Microsoft InfoPath provides application automation from code written using COM and script by using methods of the **Application** object and the **XDocuments** collection.</span></span> 
  
## <a name="overview-of-the-application-and-xdocument-objects"></a><span data-ttu-id="52750-105">アプリケーションおよび XDocument オブジェクトの概要</span><span class="sxs-lookup"><span data-stu-id="52750-105">Overview of the Application and XDocument Objects</span></span>

<span data-ttu-id="52750-106">**Application** オブジェクトには、オートメーションに使用される次のメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52750-106">The **Application** object contains the following methods used for automation:</span></span> 
  
|<span data-ttu-id="52750-107">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="52750-107">**Method**</span></span>|<span data-ttu-id="52750-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="52750-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52750-109">**CacheSolution**</span><span class="sxs-lookup"><span data-stu-id="52750-109">**CacheSolution**</span></span> <br/> |<span data-ttu-id="52750-110">キャッシュ内のを調べ、必要に応じて、発行されたフォームテンプレートの場所からキャッシュを更新します。</span><span class="sxs-lookup"><span data-stu-id="52750-110">Examines the in the cache and, if necessary, updates it from the published location of the form template.</span></span>  <br/> |
|<span data-ttu-id="52750-111">**Quit**</span><span class="sxs-lookup"><span data-stu-id="52750-111">**Quit**</span></span> <br/> |<span data-ttu-id="52750-112">Microsoft Office InfoPath アプリケーションを終了します。</span><span class="sxs-lookup"><span data-stu-id="52750-112">Quits the Microsoft Office InfoPath application.</span></span>  <br/> |
|<span data-ttu-id="52750-113">**RegisterSolution**</span><span class="sxs-lookup"><span data-stu-id="52750-113">**RegisterSolution**</span></span> <br/> |<span data-ttu-id="52750-114">指定された Microsoft Office InfoPath フォーム テンプレートをインストールします。</span><span class="sxs-lookup"><span data-stu-id="52750-114">Installs the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
|<span data-ttu-id="52750-115">**UnregisterSolution**</span><span class="sxs-lookup"><span data-stu-id="52750-115">**UnregisterSolution**</span></span> <br/> |<span data-ttu-id="52750-116">指定された Microsoft Office InfoPath フォーム テンプレートをアンインストールします。</span><span class="sxs-lookup"><span data-stu-id="52750-116">Uninstalls the specified Microsoft Office InfoPath form template.</span></span>  <br/> |
   
<span data-ttu-id="52750-117">**XDocuments** コレクションには、外部の自動化に使用できる以下のメソッドが含まれています。</span><span class="sxs-lookup"><span data-stu-id="52750-117">The **XDocuments** collection contains the following methods that can be used for external automation:</span></span> 
  
|<span data-ttu-id="52750-118">**メソッド**</span><span class="sxs-lookup"><span data-stu-id="52750-118">**Method**</span></span>|<span data-ttu-id="52750-119">**説明**</span><span class="sxs-lookup"><span data-stu-id="52750-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="52750-120">**Close** メソッド</span><span class="sxs-lookup"><span data-stu-id="52750-120">**Close** method</span></span>  <br/> |<span data-ttu-id="52750-121">指定された Microsoft Office InfoPath フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="52750-121">Closes the specified Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="52750-122">**New** メソッド</span><span class="sxs-lookup"><span data-stu-id="52750-122">**New** method</span></span>  <br/> |<span data-ttu-id="52750-123">新しい Microsoft Office InfoPath フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="52750-123">Creates a new Microsoft Office InfoPath form.</span></span>  <br/> |
|<span data-ttu-id="52750-124">**NewFromSolution** メソッド</span><span class="sxs-lookup"><span data-stu-id="52750-124">**NewFromSolution** method</span></span>  <br/> |<span data-ttu-id="52750-125">指定したフォーム テンプレートに基づいて、新しい Microsoft Office InfoPath フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="52750-125">Creates a new Microsoft Office InfoPath form based on the specified form template.</span></span>  <br/> |
|<span data-ttu-id="52750-126">**NewFromSolutionWithData** メソッド</span><span class="sxs-lookup"><span data-stu-id="52750-126">**NewFromSolutionWithData** method</span></span>  <br/> |<span data-ttu-id="52750-127">指定した XML データとフォーム テンプレートを使用して、新しい Microsoft Office InfoPath フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="52750-127">Creates a new Microsoft Office InfoPath form using the specified XML data and form template.</span></span>  <br/> |
|<span data-ttu-id="52750-128">**Open** メソッド</span><span class="sxs-lookup"><span data-stu-id="52750-128">**Open** method</span></span>  <br/> |<span data-ttu-id="52750-129">指定された Microsoft Office InfoPath フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="52750-129">Opens the specified Microsoft Office InfoPath form.</span></span>  <br/> |
   
<span data-ttu-id="52750-130">外部アプリケーションから **Application** オブジェクトを使用するには、**CreateObject** 関数と InfoPath アプリケーションの ProgID ("InfoPath.Application") を使用して、InfoPath アプリケーションを表すオブジェクト変数を作成します。</span><span class="sxs-lookup"><span data-stu-id="52750-130">To use the **Application** object from an external application, you use the **CreateObject** function with the ProgID of the InfoPath application ("InfoPath.Application") to create an object variable that represents the InfoPath application.</span></span> <span data-ttu-id="52750-131">次に、**XDocuments** プロパティを使用して **XDocuments** コレクションにアクセスし、メソッドを使用して InfoPath フォームを開くか作成します。</span><span class="sxs-lookup"><span data-stu-id="52750-131">You can then use the **XDocuments** property to access the **XDocuments** collection and use its methods to open or create an InfoPath form.</span></span> <span data-ttu-id="52750-132">次の例では、Microsoft Visual Basic 6.0 または Visual Basic for Applications (VBA) プログラミング言語を使用する **Application** オブジェクトへの参照の作成を示します。</span><span class="sxs-lookup"><span data-stu-id="52750-132">The following example demonstrates the creation of a reference to the **Application** object using the Microsoft Visual Basic 6.0 or Visual Basic for Applications (VBA) programming language:</span></span> 
  
```vb
Dim objIP As Object 
 
Set objIP = CreateObject("InfoPath.Application") 
 
' Open an existing form 
objIP.XDocuments.Open ("C:\MyFolder\MyForm.xml") 
 
' Create a new form based on a form template 
objIP.XDocuments.NewFromSolution ("C:\MyFolder\MyForm.xsn") 

```

> [!NOTE]
> <span data-ttu-id="52750-133">**CreateObject** 関数は、遅延バインディングを使用してオブジェクト変数を作成するため、Visual Basic Editor ではステートメントの自動補完を利用できません。</span><span class="sxs-lookup"><span data-stu-id="52750-133">Because the **CreateObject** function creates an object variable using late binding, automatic statement completion will not be available in the Visual Basic Editor.</span></span> <span data-ttu-id="52750-134">正しい呼び出し構文の詳細については、上記の表のリンクを参照してください。</span><span class="sxs-lookup"><span data-stu-id="52750-134">Refer to the links in the preceding tables for information about the correct calling syntax.</span></span> 
  

