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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800833"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="cf27c-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="cf27c-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="cf27c-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cf27c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cf27c-105">リーフ行がテーブルのビューからのカテゴリに属する、下位の見出しを削除する、拡張テーブルのカテゴリを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="cf27c-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="cf27c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="cf27c-106">Parameters</span></span>

 <span data-ttu-id="cf27c-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="cf27c-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="cf27c-108">[in]_PbInstanceKey_パラメーターが指す、PR_INSTANCE_KEY プロパティ内のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="cf27c-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="cf27c-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="cf27c-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="cf27c-110">[in]カテゴリの見出しの行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf27c-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="cf27c-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="cf27c-111">_ulFlags_</span></span>
  
> <span data-ttu-id="cf27c-112">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf27c-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="cf27c-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="cf27c-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="cf27c-114">[out]テーブル ビューから削除された行の総数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="cf27c-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="cf27c-115">�߂�l</span><span class="sxs-lookup"><span data-stu-id="cf27c-115">Return value</span></span>

<span data-ttu-id="cf27c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="cf27c-116">S_OK</span></span> 
  
> <span data-ttu-id="cf27c-117">折りたたみ操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="cf27c-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="cf27c-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="cf27c-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="cf27c-119">_PbInstanceKey_パラメーターで指定された行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="cf27c-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="cf27c-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="cf27c-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="cf27c-121">_PbInstanceKey_パラメーターで指定された行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="cf27c-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="cf27c-122">このエラーは、代わりに MAPI_E_NOT_FOUND です。サービス プロバイダーは、いずれかを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="cf27c-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="cf27c-123">備考</span><span class="sxs-lookup"><span data-stu-id="cf27c-123">Remarks</span></span>

<span data-ttu-id="cf27c-124">**IMAPITable::CollapseRow**メソッドは、テーブルを解除し、表形式ビューから削除します。</span><span class="sxs-lookup"><span data-stu-id="cf27c-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="cf27c-125">_PbInstanceKey_パラメーターが指す、 **PR_INSTANCE_KEY**プロパティで識別される行で始まる行が折りたたまれます。</span><span class="sxs-lookup"><span data-stu-id="cf27c-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="cf27c-126">_LpulRowCount_パラメーターの内容をビューから削除された行の数が返されます。</span><span class="sxs-lookup"><span data-stu-id="cf27c-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="cf27c-127">折りたたみ操作の結果として、ビューから削除されたテーブルの行の通知が生成されません。</span><span class="sxs-lookup"><span data-stu-id="cf27c-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="cf27c-128">表示のブックマークで定義されている行が折りたたまれると、ブックマークが表示されている次の行を指すように移動します。</span><span class="sxs-lookup"><span data-stu-id="cf27c-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="cf27c-129">分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="cf27c-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="cf27c-130">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="cf27c-130">MFCMAPI reference</span></span>

<span data-ttu-id="cf27c-131">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="cf27c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="cf27c-132">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="cf27c-132">**File**</span></span>|<span data-ttu-id="cf27c-133">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="cf27c-133">**Function**</span></span>|<span data-ttu-id="cf27c-134">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="cf27c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="cf27c-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="cf27c-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="cf27c-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="cf27c-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="cf27c-137">MFCMAPI では、 **IMAPITable::CollapseRow**メソッドを使用して、テーブルのカテゴリを折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="cf27c-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cf27c-138">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf27c-138">See also</span></span>



[<span data-ttu-id="cf27c-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="cf27c-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="cf27c-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="cf27c-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="cf27c-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="cf27c-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="cf27c-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="cf27c-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="cf27c-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="cf27c-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="cf27c-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="cf27c-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="cf27c-145">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="cf27c-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="cf27c-146">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="cf27c-146">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

