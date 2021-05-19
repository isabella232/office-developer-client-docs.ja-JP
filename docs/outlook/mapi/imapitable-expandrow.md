---
title: IMAPITableExpandRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.ExpandRow
api_type:
- COM
ms.assetid: b96dd8f6-e648-4014-8a1d-ae1da771c439
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415167"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="7322e-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="7322e-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="7322e-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7322e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7322e-105">折りたたみテーブル カテゴリを展開し、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブル ビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="7322e-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
```cpp
HRESULT ExpandRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulRowCount,
ULONG ulFlags,
LPSRowSet FAR * lppRows,
ULONG FAR * lpulMoreRows
);
```

## <a name="parameters"></a><span data-ttu-id="7322e-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="7322e-106">Parameters</span></span>

 <span data-ttu-id="7322e-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="7322e-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="7322e-108">[in]  _pbInstanceKey_ パラメーターがPR_INSTANCE_KEYするプロパティのバイト数。</span><span class="sxs-lookup"><span data-stu-id="7322e-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="7322e-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="7322e-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="7322e-110">[in]カテゴリの見出 **しPR_INSTANCE_KEY** を識別するプロパティ [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7322e-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="7322e-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="7322e-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="7322e-112">[in]  _lppRows_ パラメーターで返される行の最大数。</span><span class="sxs-lookup"><span data-stu-id="7322e-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="7322e-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7322e-113">_ulFlags_</span></span>
  
> <span data-ttu-id="7322e-114">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="7322e-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7322e-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="7322e-115">_lppRows_</span></span>
  
> <span data-ttu-id="7322e-116">[out]拡張の結果としてテーブル ビューに挿入された最初の _(ulRowCount_ まで) 行を受け取る [SRowSet](srowset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7322e-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="7322e-117">これらの行は  _、pbInstanceKey_ パラメーターで識別される見出し行の後に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="7322e-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="7322e-118">_ulRowCount パラメーターが_ 0 の場合 _、lppRows_ パラメーターは NULL になります。</span><span class="sxs-lookup"><span data-stu-id="7322e-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="7322e-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="7322e-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="7322e-120">[out]テーブル ビューに追加された行の総数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="7322e-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7322e-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="7322e-121">Return value</span></span>

<span data-ttu-id="7322e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="7322e-122">S_OK</span></span> 
  
> <span data-ttu-id="7322e-123">カテゴリが正常に展開されました。</span><span class="sxs-lookup"><span data-stu-id="7322e-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="7322e-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="7322e-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="7322e-125">_pbInstanceKey_ パラメーターで識別される行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="7322e-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="7322e-126">注釈</span><span class="sxs-lookup"><span data-stu-id="7322e-126">Remarks</span></span>

<span data-ttu-id="7322e-127">**IMAPITable::ExpandRow** メソッドは、折りたたみテーブル カテゴリを展開し、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブル ビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="7322e-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="7322e-128">_lppRows_ パラメーターで返される行数の制限は _、ulRowCount パラメーターで指定_ できます。</span><span class="sxs-lookup"><span data-stu-id="7322e-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="7322e-129">_ulRowCount_ が 0 より大きい値に設定され _、lppRows_ が指す行セットで 1 つ以上の行が返される場合、ブックマーク BOOKMARK_CURRENT の位置は、行セットの最後の行の直後の行に移動されます。</span><span class="sxs-lookup"><span data-stu-id="7322e-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="7322e-130">_ulRowCount_ を 0 に設定し、カテゴリにリーフまたは下位レベルの見出し行を追加するか、またはカテゴリにリーフまたは下位レベルの見出し行がないのでゼロ行が返される場合、BOOKMARK_CURRENT の位置は _pbInstanceKey_ で識別される行の後の行に設定されます。</span><span class="sxs-lookup"><span data-stu-id="7322e-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7322e-131">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="7322e-131">Notes to implementers</span></span>

<span data-ttu-id="7322e-132">カテゴリの展開によりテーブル ビューに追加される行に対して通知を生成しない。</span><span class="sxs-lookup"><span data-stu-id="7322e-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7322e-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="7322e-133">Notes to callers</span></span>

<span data-ttu-id="7322e-134">_lppRows_ パラメーターが指す行セット内の行数は、テーブルに実際に追加された行の数、カテゴリのリーフまたは下位レベルの見出し行のセット全体と等しくない場合があります。</span><span class="sxs-lookup"><span data-stu-id="7322e-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="7322e-135">メモリ不足や、ulRowCount パラメーターで指定された数を超えるカテゴリの行数など、エラー  _が発生する可能性_ があります。</span><span class="sxs-lookup"><span data-stu-id="7322e-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="7322e-136">どちらの場合も、BOOKMARK_CURRENT最後の行に配置されます。</span><span class="sxs-lookup"><span data-stu-id="7322e-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="7322e-137">カテゴリ内の残りの行をすぐに取得するには [、IMAPITable::QueryRows を呼び出します](imapitable-queryrows.md)。</span><span class="sxs-lookup"><span data-stu-id="7322e-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="7322e-138">カテゴリの状態が変更された場合は、テーブル通知を受け取る必要があります。</span><span class="sxs-lookup"><span data-stu-id="7322e-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="7322e-139">すべての ExpandRow 呼び出しまたは **CollapseRow** 呼び出しで更新できる行のローカル キャッシュ **を維持** できます。</span><span class="sxs-lookup"><span data-stu-id="7322e-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="7322e-140">分類テーブルの詳細については、「並べ替えと [分類」を参照してください](sorting-and-categorization.md)。</span><span class="sxs-lookup"><span data-stu-id="7322e-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7322e-141">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="7322e-141">MFCMAPI reference</span></span>

<span data-ttu-id="7322e-142">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="7322e-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7322e-143">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="7322e-143">**File**</span></span>|<span data-ttu-id="7322e-144">**関数**</span><span class="sxs-lookup"><span data-stu-id="7322e-144">**Function**</span></span>|<span data-ttu-id="7322e-145">**コメント**</span><span class="sxs-lookup"><span data-stu-id="7322e-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7322e-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="7322e-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="7322e-147">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="7322e-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="7322e-148">MFCMAPI は **IMAPITable::ExpandRow** メソッドを使用して、折りたたみテーブル カテゴリを展開します。</span><span class="sxs-lookup"><span data-stu-id="7322e-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7322e-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="7322e-149">See also</span></span>



[<span data-ttu-id="7322e-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="7322e-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="7322e-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7322e-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="7322e-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="7322e-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

