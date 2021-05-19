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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: ec305fc872d1bf1718592dabdd230617d50d3f54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434334"
---
# <a name="imapitablegetstatus"></a><span data-ttu-id="a1760-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="a1760-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="a1760-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1760-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1760-105">テーブルの状態と型を返します。</span><span class="sxs-lookup"><span data-stu-id="a1760-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="a1760-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a1760-106">Parameters</span></span>

 <span data-ttu-id="a1760-107">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="a1760-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="a1760-108">[out]テーブルの状態を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1760-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="a1760-109">次のいずれかの値を返します。</span><span class="sxs-lookup"><span data-stu-id="a1760-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="a1760-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="a1760-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="a1760-111">操作は進行中です。</span><span class="sxs-lookup"><span data-stu-id="a1760-111">No operations are in progress.</span></span>
    
<span data-ttu-id="a1760-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="a1760-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="a1760-113">テーブルの内容が予想通り変更されました。</span><span class="sxs-lookup"><span data-stu-id="a1760-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="a1760-114">この状態の値は、並べ替え操作または制限操作による変更に対して返されません。</span><span class="sxs-lookup"><span data-stu-id="a1760-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="a1760-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="a1760-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="a1760-116">[IMAPITable::Restrict 操作中にエラーが発生](imapitable-restrict.md)しました。</span><span class="sxs-lookup"><span data-stu-id="a1760-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="a1760-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="a1760-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="a1760-118">**IMAPITable::Restrict 操作** が進行中です。</span><span class="sxs-lookup"><span data-stu-id="a1760-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="a1760-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="a1760-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="a1760-120">[IMAPITable::SetColumns 操作中にエラーが発生](imapitable-setcolumns.md)しました。</span><span class="sxs-lookup"><span data-stu-id="a1760-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="a1760-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="a1760-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="a1760-122">**IMAPITable::SetColumns 操作** が進行中です。</span><span class="sxs-lookup"><span data-stu-id="a1760-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="a1760-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="a1760-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="a1760-124">[IMAPITable::SortTable 操作中にエラーが発生](imapitable-sorttable.md)しました。</span><span class="sxs-lookup"><span data-stu-id="a1760-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="a1760-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="a1760-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="a1760-126">**IMAPITable::SortTable** 操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="a1760-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="a1760-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="a1760-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="a1760-128">[out]テーブルの種類を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="a1760-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="a1760-129">次の 3 つのテーブルの種類のいずれかを返します。</span><span class="sxs-lookup"><span data-stu-id="a1760-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="a1760-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="a1760-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="a1760-131">テーブルの内容は動的です。基になるデータの変更に応じ、行と列の値が変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1760-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="a1760-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="a1760-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="a1760-133">テーブル内の行は固定されますが、これらの行内の列の値は動的であり、基になるデータが変更されるに従って変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a1760-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="a1760-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="a1760-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="a1760-135">テーブルは静的であり、基になるデータが変更された場合、その内容は変更されません。</span><span class="sxs-lookup"><span data-stu-id="a1760-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1760-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="a1760-136">Return value</span></span>

<span data-ttu-id="a1760-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="a1760-137">S_OK</span></span> 
  
> <span data-ttu-id="a1760-138">テーブルの状態が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="a1760-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a1760-139">注釈</span><span class="sxs-lookup"><span data-stu-id="a1760-139">Remarks</span></span>

<span data-ttu-id="a1760-140">**IMAPTable::GetStatus** メソッドは、テーブルの種類と現在の状態に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="a1760-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a1760-141">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="a1760-141">Notes to callers</span></span>

<span data-ttu-id="a1760-142">**GetStatus** を他の 3 つの **IMAPITable** メソッドと組み合わせて使用して、これらの操作の状態を監視し、テーブルに対する影響を判断できます。</span><span class="sxs-lookup"><span data-stu-id="a1760-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="a1760-143">次のいずれかの **IMAPITable** 呼び出しを行った後 **、GetStatus を呼び出** します。</span><span class="sxs-lookup"><span data-stu-id="a1760-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="a1760-144">[IMAPITable::制限を](imapitable-restrict.md) 設定します。</span><span class="sxs-lookup"><span data-stu-id="a1760-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="a1760-145">[IMAPITable::SortTable を使用](imapitable-sorttable.md) して並べ替え順序を確立します。</span><span class="sxs-lookup"><span data-stu-id="a1760-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="a1760-146">[IMAPITable::SetColumns を使用](imapitable-setcolumns.md) して列セットを定義します。</span><span class="sxs-lookup"><span data-stu-id="a1760-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a1760-147">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="a1760-147">MFCMAPI reference</span></span>

<span data-ttu-id="a1760-148">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a1760-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a1760-149">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="a1760-149">**File**</span></span>|<span data-ttu-id="a1760-150">**関数**</span><span class="sxs-lookup"><span data-stu-id="a1760-150">**Function**</span></span>|<span data-ttu-id="a1760-151">**コメント**</span><span class="sxs-lookup"><span data-stu-id="a1760-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a1760-152">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="a1760-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="a1760-153">CContentsTableListCtrl::GetStatus</span><span class="sxs-lookup"><span data-stu-id="a1760-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="a1760-154">MFCMAPI は **IMAPITable::GetStatus** メソッドを使用してテーブルの状態を報告します。</span><span class="sxs-lookup"><span data-stu-id="a1760-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a1760-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="a1760-155">See also</span></span>



[<span data-ttu-id="a1760-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="a1760-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="a1760-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="a1760-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="a1760-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="a1760-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="a1760-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a1760-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="a1760-160">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="a1760-160">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

