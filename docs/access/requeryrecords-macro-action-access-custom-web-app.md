---
title: RequeryRecords マクロのアクション (カスタム web アプリケーションのアクセス)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 1dab102f-24af-4984-8020-a9fb06355639
description: RequeryRecords アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。
ms.openlocfilehash: 27c6a4f62f62f6d903de7a23d2aca6db8d316a84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798724"
---
# <a name="requeryrecords-macro-action-access-custom-web-app"></a><span data-ttu-id="2dc74-103">RequeryRecords マクロのアクション (カスタム web アプリケーションのアクセス)</span><span class="sxs-lookup"><span data-stu-id="2dc74-103">RequeryRecords Macro Action (Access custom web app)</span></span>

<span data-ttu-id="2dc74-104">**RequeryRecords** アクションを使用してビューのソースに、再度、クエリを実行することで、アクティブなビュー内のデータを更新、並べ替え、およびフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="2dc74-104">You can use the **RequeryRecords** action to refresh, sort, and filter the data in the active view by requerying the source of the view.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="2dc74-p101">マイクロソフトを作成して、sharepoint web アプリケーションのアクセスを使用して不要になったをお勧めします。代わりに、web およびモバイル デバイス用のコードのないビジネス ソリューションを構築する[マイクロソフトの PowerApps](https://powerapps.microsoft.com/ja-jp/)を使用して検討してください。</span><span class="sxs-lookup"><span data-stu-id="2dc74-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/ja-jp/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="2dc74-107">設定</span><span class="sxs-lookup"><span data-stu-id="2dc74-107">Setting</span></span>

<span data-ttu-id="2dc74-108">**RequeryRecords** アクションの引数は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="2dc74-108">The **RequeryRecords** action has the following arguments.</span></span> 
  
|<span data-ttu-id="2dc74-109">**パラメーター**</span><span class="sxs-lookup"><span data-stu-id="2dc74-109">**Parameter**</span></span>|<span data-ttu-id="2dc74-110">**必須**</span><span class="sxs-lookup"><span data-stu-id="2dc74-110">**Required**</span></span>|<span data-ttu-id="2dc74-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2dc74-111">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2dc74-112">**場所 =**</span><span class="sxs-lookup"><span data-stu-id="2dc74-112">**Where=**</span></span> <br/> |<span data-ttu-id="2dc74-113">いいえ</span><span class="sxs-lookup"><span data-stu-id="2dc74-113">No</span></span>  <br/> |<span data-ttu-id="2dc74-p102">ビュー内のレコードを制限する SQL WHERE 句。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="2dc74-p102">A SQL WHERE clause that restricts the records in the view. By default, this argument is blank.</span></span>  <br/> |
|<span data-ttu-id="2dc74-116">**OrderBy**</span><span class="sxs-lookup"><span data-stu-id="2dc74-116">**OrderBy**</span></span> <br/> |<span data-ttu-id="2dc74-117">いいえ</span><span class="sxs-lookup"><span data-stu-id="2dc74-117">No</span></span>  <br/> |<span data-ttu-id="2dc74-p103">レコードを並べ替えるフィールド (複数可) の名前を含む文字列の式です。必要に応じて ASC キーワードまたは DESC キーワードを含めることもできます。既定では、この引数は空白です。</span><span class="sxs-lookup"><span data-stu-id="2dc74-p103">A string expression that includes the name of the field or fields on which to sort records and the optional ASC or DESC keywords. By default, this argument is blank.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dc74-120">注釈</span><span class="sxs-lookup"><span data-stu-id="2dc74-120">Remarks</span></span>

<span data-ttu-id="2dc74-121">**RequeryRecords** アクションが呼び出されたとき、すべての並べ替え、またはユーザーにより適用されたフィルター処理はオフにされます。</span><span class="sxs-lookup"><span data-stu-id="2dc74-121">Any sorting or filtering applied by the user is cleared when the **RequeryRecords** action is called.</span></span> 
  
<span data-ttu-id="2dc74-122">*並べ替え*引数は、フィールドまたはレコードをソートするフィールドの名前です。</span><span class="sxs-lookup"><span data-stu-id="2dc74-122">The  *OrderBy*  argument is the name of the field or fields on which you want to sort records.</span></span> <span data-ttu-id="2dc74-123">複数のフィールド名を指定する場合はコンマ (,) で区切ります。</span><span class="sxs-lookup"><span data-stu-id="2dc74-123">When you use more than one field name, separate the names with a comma (,).</span></span> 
  
<span data-ttu-id="2dc74-124">*並べ替え*引数を設定すると、既定では昇順でレコードが並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="2dc74-124">When you set the  *OrderBy*  argument, the records are sorted by default in ascending order.</span></span> 
  
<span data-ttu-id="2dc74-125">降順でレコードを並べ替えるには、 *OrderBy*の引数の式の末尾に DESC を入力します。</span><span class="sxs-lookup"><span data-stu-id="2dc74-125">To sort records in descending order, enter DESC at the end of the  *OrderBy*  argument expression.</span></span> <span data-ttu-id="2dc74-126">などの顧客レコードを取引先担当者の名前で降順に並べ替えるには、 *OrderBy*引数を"得意先コード DESC"を設定します。</span><span class="sxs-lookup"><span data-stu-id="2dc74-126">For example, to sort customer records in descending order by contact name, set the  *OrderBy*  argument to "ContactName DESC".</span></span> 
  
<span data-ttu-id="2dc74-127">降順で、姓と名の昇順で名前を並べ替えるには、」「姓 desc, FirstName ASC" *OrderBy*引数を設定します。</span><span class="sxs-lookup"><span data-stu-id="2dc74-127">To sort names by LastName descending, and FirstName ascending, set the  *OrderBy*  argument to "LastName DESC, FirstName ASC".</span></span> 
  

