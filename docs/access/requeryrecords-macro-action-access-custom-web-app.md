---
title: RequeryRecords マクロ アクション (Access カスタム Web アプリ)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: RequeryRecords アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。
ms.openlocfilehash: 69d88401abc0de417f7dc58e275c66f2037212aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439248"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="baffd-103">RequeryRecords マクロ アクション (Access カスタム Web アプリ)</span><span class="sxs-lookup"><span data-stu-id="baffd-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="baffd-104">**RequeryRecords** アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="baffd-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="baffd-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/en-us/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="baffd-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="baffd-107">設定</span><span class="sxs-lookup"><span data-stu-id="baffd-107">Setting</span></span>

<span data-ttu-id="baffd-108">**RequeryRecords** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="baffd-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="baffd-109">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="baffd-109">**Parameter**</span></span>|<span data-ttu-id="baffd-110">**必須**</span><span class="sxs-lookup"><span data-stu-id="baffd-110">**Required**</span></span>|<span data-ttu-id="baffd-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="baffd-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="baffd-112">**Where=**</span><span class="sxs-lookup"><span data-stu-id="baffd-112">**Where=**</span></span> <br/> |<span data-ttu-id="baffd-113">いいえ</span><span class="sxs-lookup"><span data-stu-id="baffd-113">No</span></span>  <br/> |<span data-ttu-id="baffd-p102">ビュー内のレコードを制限する SQL WHERE 句。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="baffd-p102">A SQL WHERE clause that restricts the records in the view. By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="baffd-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="baffd-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="baffd-117">いいえ</span><span class="sxs-lookup"><span data-stu-id="baffd-117">No</span></span>  <br/> |<span data-ttu-id="baffd-p103">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="baffd-p103">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords. By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baffd-120">注釈</span><span class="sxs-lookup"><span data-stu-id="baffd-120">Remarks</span></span>

<span data-ttu-id="baffd-121">**RequeryRecords** アクションが呼び出されたとき、すべての並べ替え、またはユーザーにより適用されたフィルター処理はオフにされます。</span><span class="sxs-lookup"><span data-stu-id="baffd-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="baffd-p104">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span><span class="sxs-lookup"><span data-stu-id="baffd-p104">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records. When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="baffd-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span><span class="sxs-lookup"><span data-stu-id="baffd-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="baffd-p105">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression. For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span><span class="sxs-lookup"><span data-stu-id="baffd-p105">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression. For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="baffd-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span><span class="sxs-lookup"><span data-stu-id="baffd-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

