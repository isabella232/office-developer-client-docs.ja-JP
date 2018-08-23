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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 48ca692779fb53cab386d8a18b5f0a50e11d531c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569436"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="18f63-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="18f63-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="18f63-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18f63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18f63-105">テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="18f63-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="18f63-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="18f63-106">Parameters</span></span>

 <span data-ttu-id="18f63-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="18f63-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="18f63-108">[out]現在の並べ替え順序を保持する[SSortOrderSet](ssortorderset.md)の構造体へのポインターへのポインター。</span><span class="sxs-lookup"><span data-stu-id="18f63-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18f63-109">�߂�l</span><span class="sxs-lookup"><span data-stu-id="18f63-109">Return value</span></span>

<span data-ttu-id="18f63-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="18f63-110">S_OK</span></span> 
  
> <span data-ttu-id="18f63-111">現在の並べ替え順序が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="18f63-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="18f63-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="18f63-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="18f63-113">別の操作は、並べ替え順の取得操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="18f63-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="18f63-114">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="18f63-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18f63-115">注釈</span><span class="sxs-lookup"><span data-stu-id="18f63-115">Remarks</span></span>

<span data-ttu-id="18f63-116">**IMAPITable::QuerySortOrder**メソッドは、テーブルの現在の並べ替え順序を取得します。</span><span class="sxs-lookup"><span data-stu-id="18f63-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="18f63-117">[SSortOrderSet](ssortorderset.md)構造体のソート順を説明しています。</span><span class="sxs-lookup"><span data-stu-id="18f63-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="18f63-118">場合、 **cSorts** 、 **SSortOrderSet**構造体のメンバーを 0 に設定できます。</span><span class="sxs-lookup"><span data-stu-id="18f63-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="18f63-119">表はソートされていません。</span><span class="sxs-lookup"><span data-stu-id="18f63-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="18f63-120">テーブルの並べ替え方法に関する情報はありません。</span><span class="sxs-lookup"><span data-stu-id="18f63-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="18f63-121">**SSortOrderSet**構造体は、並べ替えの順序を記述するための適切ではありません。</span><span class="sxs-lookup"><span data-stu-id="18f63-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="18f63-122">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="18f63-122">Notes to implementers</span></span>

<span data-ttu-id="18f63-123">呼び出しされた場合、 [IMAPITable::SortTable](imapitable-sorttable.md)メソッドに並べ替えキーの列を含む**SSortOrderSet**構造を持つ、現在の並べ替え順序を削除し、いずれかを使用する必要がある場合は、既定の順序を適用します。</span><span class="sxs-lookup"><span data-stu-id="18f63-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="18f63-124">**QuerySortOrder**に以降の呼び出しでは、並べ替えキーの 0 個以上の列を返すかどうかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="18f63-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="18f63-125">現在のビューより多くの列を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="18f63-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="18f63-126">並べ替えの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="18f63-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="18f63-127">関連項目</span><span class="sxs-lookup"><span data-stu-id="18f63-127">See also</span></span>



[<span data-ttu-id="18f63-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="18f63-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="18f63-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="18f63-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="18f63-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="18f63-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="18f63-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="18f63-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

