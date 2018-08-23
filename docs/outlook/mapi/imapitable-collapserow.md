---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b4dd7e9715c2d3c99eda44f7eed0b3360a2e33be
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595301"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="b545d-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="b545d-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="b545d-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b545d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b545d-105">リーフ行がテーブルのビューからのカテゴリに属する、下位の見出しを削除する、拡張テーブルのカテゴリを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b545d-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="b545d-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b545d-106">Parameters</span></span>

 <span data-ttu-id="b545d-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="b545d-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="b545d-108">[in]_PbInstanceKey_パラメーターが指す、PR_INSTANCE_KEY プロパティ内のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="b545d-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="b545d-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="b545d-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="b545d-110">[in]カテゴリの見出しの行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b545d-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="b545d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b545d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="b545d-112">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b545d-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b545d-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="b545d-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="b545d-114">[out]テーブル ビューから削除された行の総数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b545d-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b545d-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b545d-115">Return value</span></span>

<span data-ttu-id="b545d-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b545d-116">S_OK</span></span> 
  
> <span data-ttu-id="b545d-117">折りたたみ操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="b545d-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="b545d-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b545d-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b545d-119">_PbInstanceKey_パラメーターで指定された行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="b545d-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="b545d-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="b545d-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="b545d-121">_PbInstanceKey_パラメーターで指定された行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="b545d-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="b545d-122">このエラーは、代わりに MAPI_E_NOT_FOUND です。サービス プロバイダーは、いずれかを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="b545d-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b545d-123">注釈</span><span class="sxs-lookup"><span data-stu-id="b545d-123">Remarks</span></span>

<span data-ttu-id="b545d-124">**IMAPITable::CollapseRow**メソッドは、テーブルを解除し、表形式ビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="b545d-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="b545d-125">_PbInstanceKey_パラメーターが指す、 **PR_INSTANCE_KEY**プロパティで識別される行で始まる行が折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="b545d-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="b545d-126">_LpulRowCount_パラメーターの内容をビューから削除された行の数が返されます。</span><span class="sxs-lookup"><span data-stu-id="b545d-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="b545d-127">折りたたみ操作の結果として、ビューから削除されたテーブルの行の通知が生成されません。</span><span class="sxs-lookup"><span data-stu-id="b545d-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="b545d-128">表示のブックマークで定義されている行が折りたたまれると、ブックマークが表示されている次の行を指すように移動します。</span><span class="sxs-lookup"><span data-stu-id="b545d-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="b545d-129">分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b545d-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b545d-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="b545d-130">MFCMAPI reference</span></span>

<span data-ttu-id="b545d-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="b545d-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b545d-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="b545d-132">**File**</span></span>|<span data-ttu-id="b545d-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="b545d-133">**Function**</span></span>|<span data-ttu-id="b545d-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="b545d-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b545d-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="b545d-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b545d-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="b545d-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="b545d-137">MFCMAPI では、 **IMAPITable::CollapseRow**メソッドを使用して、テーブルのカテゴリを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="b545d-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b545d-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="b545d-138">See also</span></span>



[<span data-ttu-id="b545d-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b545d-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="b545d-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="b545d-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="b545d-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="b545d-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="b545d-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="b545d-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="b545d-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="b545d-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="b545d-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="b545d-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="b545d-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b545d-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="b545d-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b545d-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

