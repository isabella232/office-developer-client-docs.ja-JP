---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407551"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="f2129-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="f2129-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="f2129-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2129-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2129-105">テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2129-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="f2129-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f2129-106">Parameters</span></span>

 <span data-ttu-id="f2129-107">_lppsortcriteria_</span><span class="sxs-lookup"><span data-stu-id="f2129-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="f2129-108">読み上げ現在の並べ替え順序を保持する[ssortorderset](ssortorderset.md)構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f2129-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f2129-109">戻り値</span><span class="sxs-lookup"><span data-stu-id="f2129-109">Return value</span></span>

<span data-ttu-id="f2129-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2129-110">S_OK</span></span> 
  
> <span data-ttu-id="f2129-111">現在の並べ替え順序が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="f2129-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="f2129-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f2129-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f2129-113">別の操作が進行中であるため、並べ替え順序の取得操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="f2129-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="f2129-114">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f2129-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2129-115">注釈</span><span class="sxs-lookup"><span data-stu-id="f2129-115">Remarks</span></span>

<span data-ttu-id="f2129-116">**IMAPITable:: querysortorder**メソッドは、テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="f2129-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="f2129-117">並べ替え順序は、 [ssortorderset](ssortorderset.md)構造で記述されます。</span><span class="sxs-lookup"><span data-stu-id="f2129-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="f2129-118">次\*\*\*\* の場合、 **ssortorderset**構造の csortmember は0に設定できます。</span><span class="sxs-lookup"><span data-stu-id="f2129-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="f2129-119">表は並べ替えられていません。</span><span class="sxs-lookup"><span data-stu-id="f2129-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="f2129-120">表の並べ替え方法に関する情報はありません。</span><span class="sxs-lookup"><span data-stu-id="f2129-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="f2129-121">**ssortorderset**構造は、並べ替え順序の記述には適していません。</span><span class="sxs-lookup"><span data-stu-id="f2129-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="f2129-122">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f2129-122">Notes to implementers</span></span>

<span data-ttu-id="f2129-123">[IMAPITable:: sorttable](imapitable-sorttable.md)メソッドに対して、列に0を含む**ssortorderset**構造が設定されている場合は、現在の並べ替え順序を削除し、既定の順序 (存在する場合) を適用します。</span><span class="sxs-lookup"><span data-stu-id="f2129-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="f2129-124">以降の**querysortorder**の呼び出しでは、並べ替えキーに0個以上の列を返すかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f2129-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="f2129-125">現在のビューの数を超える列を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="f2129-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="f2129-126">並べ替えの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f2129-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2129-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="f2129-127">See also</span></span>



[<span data-ttu-id="f2129-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="f2129-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="f2129-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f2129-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="f2129-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="f2129-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="f2129-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2129-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

