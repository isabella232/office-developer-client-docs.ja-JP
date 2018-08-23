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
ms.openlocfilehash: 1b3d8c74d85696e733b378a4cac2b8e2a3b6a072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800823"
---
# <a name="imapitableexpandrow"></a><span data-ttu-id="ecccf-103">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="ecccf-103">IMAPITable::ExpandRow</span></span>

  
  
<span data-ttu-id="ecccf-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ecccf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ecccf-105">リーフまたは表形式ビューをカテゴリに属している下位レベルの見出しの行を追加する、折りたたまれているテーブルのカテゴリを展開します。</span><span class="sxs-lookup"><span data-stu-id="ecccf-105">Expands a collapsed table category, adding the leaf or lower-level heading rows belonging to the category to the table view.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="ecccf-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ecccf-106">Parameters</span></span>

 <span data-ttu-id="ecccf-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ecccf-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="ecccf-108">[in]_PbInstanceKey_パラメーターが指す、PR_INSTANCE_KEY プロパティ内のバイト数です。</span><span class="sxs-lookup"><span data-stu-id="ecccf-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="ecccf-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="ecccf-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="ecccf-110">[in]カテゴリの見出しの行を識別する**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) のプロパティへのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecccf-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="ecccf-111">_ulRowCount_</span><span class="sxs-lookup"><span data-stu-id="ecccf-111">_ulRowCount_</span></span>
  
> <span data-ttu-id="ecccf-112">[in]_LppRows_パラメーターに返す行の最大数です。</span><span class="sxs-lookup"><span data-stu-id="ecccf-112">[in] The maximum number of rows to return in the  _lppRows_ parameter.</span></span> 
    
 <span data-ttu-id="ecccf-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ecccf-113">_ulFlags_</span></span>
  
> <span data-ttu-id="ecccf-114">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ecccf-114">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="ecccf-115">_lppRows_</span><span class="sxs-lookup"><span data-stu-id="ecccf-115">_lppRows_</span></span>
  
> <span data-ttu-id="ecccf-116">[out]拡張の結果としてテーブルのビューに挿入されている ( _ulRowCount_) までの最初のローを受信する[SRowSet](srowset.md)構造体へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecccf-116">[out] A pointer to an [SRowSet](srowset.md) structure receiving the first (up to  _ulRowCount_) rows that have been inserted into the table view as a result of the expansion.</span></span> <span data-ttu-id="ecccf-117">_PbInstanceKey_パラメーターで指定された見出しの行の後は、これらの行が挿入されます。</span><span class="sxs-lookup"><span data-stu-id="ecccf-117">These rows are inserted after the heading row identified by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="ecccf-118">_LppRows_パラメーターは、 _ulRowCount_パラメーターが 0 の場合、NULL にすることができます。</span><span class="sxs-lookup"><span data-stu-id="ecccf-118">The  _lppRows_ parameter can be NULL if the  _ulRowCount_ parameter is zero.</span></span> 
    
 <span data-ttu-id="ecccf-119">_lpulMoreRows_</span><span class="sxs-lookup"><span data-stu-id="ecccf-119">_lpulMoreRows_</span></span>
  
> <span data-ttu-id="ecccf-120">[out]テーブル ビューに追加された行の総数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="ecccf-120">[out] A pointer to the total number of rows that were added to the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ecccf-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="ecccf-121">Return value</span></span>

<span data-ttu-id="ecccf-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="ecccf-122">S_OK</span></span> 
  
> <span data-ttu-id="ecccf-123">カテゴリは正常に展開されています。</span><span class="sxs-lookup"><span data-stu-id="ecccf-123">The category was expanded successfully.</span></span>
    
<span data-ttu-id="ecccf-124">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="ecccf-124">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="ecccf-125">_PbInstanceKey_パラメーターで指定された行が存在しません。</span><span class="sxs-lookup"><span data-stu-id="ecccf-125">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="ecccf-126">注釈</span><span class="sxs-lookup"><span data-stu-id="ecccf-126">Remarks</span></span>

<span data-ttu-id="ecccf-127">**IMAPITable::ExpandRow**メソッドでは、リーフやテーブル ・ ビューをカテゴリに属している下位レベルの見出しの行を追加する、折りたたまれているテーブルのカテゴリを展開します。</span><span class="sxs-lookup"><span data-stu-id="ecccf-127">The **IMAPITable::ExpandRow** method expands a collapsed table category, adding the leaf or lower-level heading rows that belong to the category to the table view.</span></span> <span data-ttu-id="ecccf-128">_LppRows_パラメーターで返される行の数に制限は、 _ulRowCount_パラメーターで指定できます。</span><span class="sxs-lookup"><span data-stu-id="ecccf-128">A limit to the number of rows to be returned in the  _lppRows_ parameter can be specified in the  _ulRowCount_ parameter.</span></span> <span data-ttu-id="ecccf-129">_UlRowCount_が 0 より大きい値に設定すると、 _lppRows_で指定された行セットの 1 つまたは複数の行が返されます、BOOKMARK_CURRENT は、行の最後の行の直後の行に移動するブックマークの位置を設定します。</span><span class="sxs-lookup"><span data-stu-id="ecccf-129">When  _ulRowCount_ is set to a value greater than zero and one or more rows are returned in the row set pointed to by  _lppRows_, the position of the bookmark BOOKMARK_CURRENT is moved to the row immediately following the last row in the row set.</span></span>
  
<span data-ttu-id="ecccf-130">行に BOOKMARK_CURRENT の位置を設定するカテゴリに追加する_ulRowCount_を 0 に設定すると、リーフは 0、または下位の見出し行を要求するか、リーフまたはカテゴリ内の下位レベルの見出しの行がないために、0 個の行が返されます、次の_pbInstanceKey_で識別される行です。</span><span class="sxs-lookup"><span data-stu-id="ecccf-130">When  _ulRowCount_ is set to zero, requesting that zero leaf or lower-level heading rows be added to the category, or zero rows are returned because there are no leaf or lower-level heading rows in the category, the position of BOOKMARK_CURRENT is set to the row following the row identified by  _pbInstanceKey_.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ecccf-131">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="ecccf-131">Notes to implementers</span></span>

<span data-ttu-id="ecccf-132">カテゴリの拡張のためのテーブル ビューに追加される行に通知を生成しません。</span><span class="sxs-lookup"><span data-stu-id="ecccf-132">Do not generate notifications on rows that are added to a table view due to category expansion.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="ecccf-133">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="ecccf-133">Notes to callers</span></span>

<span data-ttu-id="ecccf-134">_LppRows_パラメーターで指定された行セット内の行の数ではテーブルに実際に追加された行の数が等しくない場合がありますが、全体のリーフの設定または下位の見出し行のカテゴリ。</span><span class="sxs-lookup"><span data-stu-id="ecccf-134">The number of rows in the row set pointed to by the  _lppRows_ parameter might not equal the number of rows that were actually added to the table, the entire set of leaf or lower-level heading rows for the category.</span></span> <span data-ttu-id="ecccf-135">メモリ不足、または_ulRowCount_パラメーターで指定された数を超えるカテゴリ内の行の数などは、エラーが発生することができます。</span><span class="sxs-lookup"><span data-stu-id="ecccf-135">Errors can occur, such as insufficient memory, or the number of rows in the category exceeding the number specified in  _ulRowCount_ parameter.</span></span> <span data-ttu-id="ecccf-136">BOOKMARK_CURRENT は、いずれの場合も、返された最後の行に配置されます。</span><span class="sxs-lookup"><span data-stu-id="ecccf-136">In either case, BOOKMARK_CURRENT will be positioned at the last row returned.</span></span> <span data-ttu-id="ecccf-137">カテゴリ内の行の残りの部分をすぐに取得するには、 [IMAPITable::QueryRows](imapitable-queryrows.md)を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ecccf-137">To immediately retrieve the rest of the rows in the category, call [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span>
  
<span data-ttu-id="ecccf-138">カテゴリの状態を変更するとテーブルの通知が受信されないようにします。</span><span class="sxs-lookup"><span data-stu-id="ecccf-138">Do not expect to receive a table notification when a category changes its state.</span></span> <span data-ttu-id="ecccf-139">**ExpandRow**または**CollapseRow**呼び出しのたびに更新される行のローカル キャッシュを保持することができます。</span><span class="sxs-lookup"><span data-stu-id="ecccf-139">You can maintain a local cache of rows that can be updated with every **ExpandRow** or **CollapseRow** call.</span></span> 
  
<span data-ttu-id="ecccf-140">分類されたテーブルの詳細については、[並べ替えや分類](sorting-and-categorization.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ecccf-140">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ecccf-141">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="ecccf-141">MFCMAPI reference</span></span>

<span data-ttu-id="ecccf-142">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="ecccf-142">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ecccf-143">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="ecccf-143">**File**</span></span>|<span data-ttu-id="ecccf-144">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="ecccf-144">**Function**</span></span>|<span data-ttu-id="ecccf-145">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="ecccf-145">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ecccf-146">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="ecccf-146">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="ecccf-147">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="ecccf-147">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="ecccf-148">MFCMAPI では、 **IMAPITable::ExpandRow**メソッドを使用して、折りたたまれているテーブルのカテゴリを展開します。</span><span class="sxs-lookup"><span data-stu-id="ecccf-148">MFCMAPI uses the **IMAPITable::ExpandRow** method to expand a collapsed table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ecccf-149">関連項目</span><span class="sxs-lookup"><span data-stu-id="ecccf-149">See also</span></span>



[<span data-ttu-id="ecccf-150">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="ecccf-150">IMAPITable::CollapseRow</span></span>](imapitable-collapserow.md)
  
[<span data-ttu-id="ecccf-151">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecccf-151">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="ecccf-152">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="ecccf-152">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

