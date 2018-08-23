---
title: IMAPITableGetStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetStatus
api_type:
- COM
ms.assetid: f114f1fa-bc05-4587-875b-71548c5912ea
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 6478f2c6c8196fa332a7b019269e6a6266485d1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800849"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="bb233-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="bb233-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="bb233-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb233-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bb233-105">テーブルのステータスおよび種類を返します。</span><span class="sxs-lookup"><span data-stu-id="bb233-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="bb233-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bb233-106">Parameters</span></span>

 <span data-ttu-id="bb233-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="bb233-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="bb233-108">[out]テーブルのステータスを示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb233-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="bb233-109">次の値のいずれかが返されます。</span><span class="sxs-lookup"><span data-stu-id="bb233-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="bb233-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="bb233-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="bb233-111">操作が進行中ではありません。</span><span class="sxs-lookup"><span data-stu-id="bb233-111">No operations are in progress.</span></span>
    
<span data-ttu-id="bb233-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="bb233-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="bb233-113">テーブルの内容が変更された expectantly。</span><span class="sxs-lookup"><span data-stu-id="bb233-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="bb233-114">並べ替えまたは制限の操作に起因する変更は、このステータス値は返されません。</span><span class="sxs-lookup"><span data-stu-id="bb233-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="bb233-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="bb233-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="bb233-116">[IMAPITable::Restrict](imapitable-restrict.md)操作中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="bb233-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="bb233-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="bb233-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="bb233-118">**IMAPITable::Restrict**操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="bb233-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="bb233-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="bb233-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="bb233-120">[IMAPITable::SetColumns](imapitable-setcolumns.md)操作中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="bb233-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="bb233-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="bb233-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="bb233-122">**IMAPITable::SetColumns**操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="bb233-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="bb233-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="bb233-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="bb233-124">[IMAPITable::SortTable](imapitable-sorttable.md)操作中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="bb233-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="bb233-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="bb233-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="bb233-126">**IMAPITable::SortTable**操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="bb233-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="bb233-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="bb233-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="bb233-128">[out]テーブルのタイプを示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="bb233-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="bb233-129">次の 3 つのテーブルの種類のいずれかが返されます。</span><span class="sxs-lookup"><span data-stu-id="bb233-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="bb233-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="bb233-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="bb233-131">テーブルの内容は動的です。行と列の値は、基になるデータの変化に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="bb233-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="bb233-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="bb233-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="bb233-133">テーブル内の行は固定ですが、これらの行に列の値は動的で、基になるデータの変化に応じて変更できます。</span><span class="sxs-lookup"><span data-stu-id="bb233-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="bb233-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="bb233-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="bb233-135">テーブルは、静的および基になるデータが変更されたとき、その内容が変更されません。</span><span class="sxs-lookup"><span data-stu-id="bb233-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bb233-136">�߂�l</span><span class="sxs-lookup"><span data-stu-id="bb233-136">Return value</span></span>

<span data-ttu-id="bb233-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb233-137">S_OK</span></span> 
  
> <span data-ttu-id="bb233-138">テーブルの状態が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="bb233-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bb233-139">注釈</span><span class="sxs-lookup"><span data-stu-id="bb233-139">Remarks</span></span>

<span data-ttu-id="bb233-140">**IMAPTable::GetStatus**メソッドは、テーブルの種類と現在の状態に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="bb233-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bb233-141">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="bb233-141">Notes to callers</span></span>

<span data-ttu-id="bb233-142">ほかの 3 つの**IMAPITable**メソッドと組み合わせて**GetStatus**を使用するにはこれらの操作の状態を監視し、テーブル上の効果を確認します。</span><span class="sxs-lookup"><span data-stu-id="bb233-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="bb233-143">**IMAPITable**呼び出しを次のいずれかを行った後に、 **GetStatus**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="bb233-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="bb233-144">[IMAPITable::Restrict](imapitable-restrict.md)の制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="bb233-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="bb233-145">[IMAPITable::SortTable](imapitable-sorttable.md)の並べ替え順序を確立します。</span><span class="sxs-lookup"><span data-stu-id="bb233-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="bb233-146">列を定義するのには[IMAPITable::SetColumns](imapitable-setcolumns.md)を設定します。</span><span class="sxs-lookup"><span data-stu-id="bb233-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bb233-147">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="bb233-147">MFCMAPI reference</span></span>

<span data-ttu-id="bb233-148">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="bb233-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bb233-149">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="bb233-149">**File**</span></span>|<span data-ttu-id="bb233-150">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="bb233-150">**Function**</span></span>|<span data-ttu-id="bb233-151">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="bb233-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bb233-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="bb233-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="bb233-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="bb233-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="bb233-154">MFCMAPI では、 **IMAPITable::GetStatus**メソッドを使用して、テーブルのステータスを報告します。</span><span class="sxs-lookup"><span data-stu-id="bb233-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb233-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="bb233-155">See also</span></span>



[<span data-ttu-id="bb233-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="bb233-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="bb233-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="bb233-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="bb233-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="bb233-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="bb233-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb233-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="bb233-160">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="bb233-160">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

