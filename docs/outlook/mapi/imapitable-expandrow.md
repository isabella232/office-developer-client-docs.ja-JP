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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 5e2ce756baaefef7bd0028e746b1dbe10756365e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329043"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="b2c9f-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="b2c9f-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="b2c9f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b2c9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b2c9f-105">折りたたまれたテーブルカテゴリを展開して、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブルビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b2c9f-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b2c9f-106">Parameters</span></span>

 <span data-ttu-id="b2c9f-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="b2c9f-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="b2c9f-108">順番_pbInstanceKey_パラメーターが指す PR_INSTANCE_KEY プロパティのバイト数。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="b2c9f-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="b2c9f-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="b2c9f-110">順番カテゴリの見出し行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="b2c9f-111">_ulrowcount_</span><span class="sxs-lookup"><span data-stu-id="b2c9f-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="b2c9f-112">順番_lpprows_パラメーターで取得する行の最大数。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="b2c9f-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b2c9f-113">_ulFlags_</span></span>
  
> <span data-ttu-id="b2c9f-114">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="b2c9f-115">_lpprows_</span><span class="sxs-lookup"><span data-stu-id="b2c9f-115">_lppRows_</span></span>
  
> <span data-ttu-id="b2c9f-116">読み上げ拡張の結果としてテーブルビューに挿入された最初の (最大_ulrowcount_) 行を受信する[srowset](srowset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="b2c9f-117">これらの行は、 _pbInstanceKey_パラメーターによって指定される見出し行の後に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="b2c9f-118">_ulrowcount_パラメーターが0の場合は、 _lpprows_パラメーターを NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="b2c9f-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="b2c9f-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="b2c9f-120">読み上げテーブルビューに追加された行の合計数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b2c9f-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="b2c9f-121">Return value</span></span>

<span data-ttu-id="b2c9f-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b2c9f-122">S_OK</span></span> 
  
> <span data-ttu-id="b2c9f-123">カテゴリが正常に展開されました。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="b2c9f-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="b2c9f-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="b2c9f-125">_pbInstanceKey_パラメーターで指定された行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="b2c9f-126">解説</span><span class="sxs-lookup"><span data-stu-id="b2c9f-126">Remarks</span></span>

<span data-ttu-id="b2c9f-127">**IMAPITable:: expandrow**メソッドは、折りたたまれたテーブルカテゴリを展開し、そのカテゴリに属するリーフまたは下位レベルの見出し行をテーブルビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="b2c9f-128">_lpprows_パラメーターで返される行数の制限は、 _ulrowcount_パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="b2c9f-129">_ulrowcount_が0より大きい値に設定されている場合に、 _lpprows_が指す行セットで1つ以上の行が返されると、bookmark BOOKMARK_CURRENT の位置は、行セットの最後の行の直後の行に移動します。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="b2c9f-130">_ulrowcount_が0に設定されている場合、0個のリーフまたは下位レベルの見出し行をカテゴリに追加することを要求するか、カテゴリにリーフまたは下位レベルの見出し行がないために0行が返される場合、BOOKMARK_CURRENT の位置は行に設定されます。_pbInstanceKey_によって識別される行の次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b2c9f-131">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="b2c9f-131">Notes to implementers</span></span>

<span data-ttu-id="b2c9f-132">カテゴリの拡張によってテーブルビューに追加された行に対して通知を生成しません。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b2c9f-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="b2c9f-133">Notes to callers</span></span>

<span data-ttu-id="b2c9f-134">_lpprows_パラメーターによって指定された行セット内の行数が、そのカテゴリのリーフまたは下位レベルの見出し行のセット全体で、実際にテーブルに追加された行数と一致しない場合があります。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="b2c9f-135">メモリが不足しているなどのエラー、または_ulrowcount_パラメーターで指定された数を超えるカテゴリ内の行の数が発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="b2c9f-136">どちらの場合でも、BOOKMARK_CURRENT は返された最後の行に配置されます。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="b2c9f-137">カテゴリ内の残りの行をすぐに取得するには、「 [IMAPITable:: QueryRows](imapitable-queryrows.md)」という呼び出しを行います。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="b2c9f-138">カテゴリの状態が変更されたときに、テーブル通知を受け取ることはありません。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="b2c9f-139">すべての**expandrow**または**CollapseRow**呼び出しで更新できる行のローカルキャッシュを維持できます。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="b2c9f-140">カテゴリ別テーブルの詳細については、「[並べ替えと分類](sorting-and-categorization.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b2c9f-141">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="b2c9f-141">MFCMAPI reference</span></span>

<span data-ttu-id="b2c9f-142">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b2c9f-143">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="b2c9f-143">**File**</span></span>|<span data-ttu-id="b2c9f-144">**関数**</span><span class="sxs-lookup"><span data-stu-id="b2c9f-144">**Function**</span></span>|<span data-ttu-id="b2c9f-145">**コメント**</span><span class="sxs-lookup"><span data-stu-id="b2c9f-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b2c9f-146">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="b2c9f-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="b2c9f-147">CContentsTableListCtrl::D oexpandcollapse</span><span class="sxs-lookup"><span data-stu-id="b2c9f-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="b2c9f-148">mfcmapi は、 **IMAPITable:: expandrow**メソッドを使用して、折りたたまれたテーブルカテゴリを展開します。</span><span class="sxs-lookup"><span data-stu-id="b2c9f-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2c9f-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2c9f-149">See also</span></span>



[<span data-ttu-id="b2c9f-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="b2c9f-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="b2c9f-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b2c9f-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="b2c9f-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="b2c9f-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

