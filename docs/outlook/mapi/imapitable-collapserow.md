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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416175"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="56f98-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="56f98-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="56f98-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56f98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56f98-105">展開されたテーブル カテゴリを折りたたみ、そのカテゴリに属する下位レベルの見出しとリーフ行をテーブル ビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="56f98-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="56f98-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="56f98-106">Parameters</span></span>

 <span data-ttu-id="56f98-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="56f98-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="56f98-108">[in]  _pbInstanceKey_ パラメーターがPR_INSTANCE_KEYするプロパティのバイト数。</span><span class="sxs-lookup"><span data-stu-id="56f98-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="56f98-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="56f98-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="56f98-110">[in]カテゴリの見出 **しPR_INSTANCE_KEY** を識別するプロパティ [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)へのポインター。</span><span class="sxs-lookup"><span data-stu-id="56f98-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="56f98-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="56f98-111">_ulFlags_</span></span>
  
> <span data-ttu-id="56f98-112">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="56f98-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="56f98-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="56f98-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="56f98-114">[out]テーブル ビューから削除される行の総数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="56f98-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="56f98-115">戻り値</span><span class="sxs-lookup"><span data-stu-id="56f98-115">Return value</span></span>

<span data-ttu-id="56f98-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="56f98-116">S_OK</span></span> 
  
> <span data-ttu-id="56f98-117">折りたたみ操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="56f98-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="56f98-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="56f98-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="56f98-119">_pbInstanceKey_ パラメーターで識別される行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="56f98-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="56f98-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="56f98-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="56f98-121">_pbInstanceKey_ パラメーターで識別される行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="56f98-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="56f98-122">このエラーは、このエラーの代わりにMAPI_E_NOT_FOUND。サービス プロバイダーは、どちらか 1 つを返す場合があります。</span><span class="sxs-lookup"><span data-stu-id="56f98-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="56f98-123">注釈</span><span class="sxs-lookup"><span data-stu-id="56f98-123">Remarks</span></span>

<span data-ttu-id="56f98-124">**IMAPITable::CollapseRow** メソッドは、テーブル カテゴリを折りたたみ、テーブル ビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="56f98-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="56f98-125">行は _、pbInstanceKey_ パラメーターが指す **PR_INSTANCE_KEYプロパティで** 識別される行から折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="56f98-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="56f98-126">ビューから削除された行の数は  _、lpulRowCount_ パラメーターの内容で返されます。</span><span class="sxs-lookup"><span data-stu-id="56f98-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="56f98-127">折りたたみ操作の結果としてビューから削除されたテーブル行に対する通知は生成されません。</span><span class="sxs-lookup"><span data-stu-id="56f98-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="56f98-128">ブックマークによって定義された行が表示されない状態で折りたたむ場合、ブックマークは次に表示される行を指す位置に移動されます。</span><span class="sxs-lookup"><span data-stu-id="56f98-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="56f98-129">分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。</span><span class="sxs-lookup"><span data-stu-id="56f98-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="56f98-130">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="56f98-130">MFCMAPI reference</span></span>

<span data-ttu-id="56f98-131">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="56f98-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="56f98-132">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="56f98-132">**File**</span></span>|<span data-ttu-id="56f98-133">**関数**</span><span class="sxs-lookup"><span data-stu-id="56f98-133">**Function**</span></span>|<span data-ttu-id="56f98-134">**コメント**</span><span class="sxs-lookup"><span data-stu-id="56f98-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56f98-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="56f98-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="56f98-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="56f98-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="56f98-137">MFCMAPI では **、IMAPITable::CollapseRow** メソッドを使用してテーブル カテゴリを折りたたむ。</span><span class="sxs-lookup"><span data-stu-id="56f98-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="56f98-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="56f98-138">See also</span></span>



[<span data-ttu-id="56f98-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="56f98-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="56f98-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="56f98-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="56f98-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="56f98-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="56f98-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="56f98-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="56f98-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="56f98-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="56f98-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="56f98-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="56f98-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="56f98-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="56f98-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="56f98-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

