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
# <a name="imapitablegetstatus"></a><span data-ttu-id="9de83-103">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="9de83-103">IMAPITable::GetStatus</span></span>

  
  
<span data-ttu-id="9de83-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9de83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9de83-105">テーブルの状態と種類を返します。</span><span class="sxs-lookup"><span data-stu-id="9de83-105">Returns the table's status and type.</span></span>
  
```cpp
HRESULT GetStatus(
ULONG FAR * lpulTableStatus,
ULONG FAR * lpulTableType
);
```

## <a name="parameters"></a><span data-ttu-id="9de83-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9de83-106">Parameters</span></span>

 <span data-ttu-id="9de83-107">_lpultablestatus_</span><span class="sxs-lookup"><span data-stu-id="9de83-107">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="9de83-108">読み上げテーブルの状態を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9de83-108">[out] Pointer to a value indicating the status of the table.</span></span> <span data-ttu-id="9de83-109">次のいずれかの値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="9de83-109">One of the following values can be returned:</span></span>
    
<span data-ttu-id="9de83-110">TBLSTAT_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="9de83-110">TBLSTAT_COMPLETE</span></span> 
  
> <span data-ttu-id="9de83-111">進行中の操作はありません。</span><span class="sxs-lookup"><span data-stu-id="9de83-111">No operations are in progress.</span></span>
    
<span data-ttu-id="9de83-112">TBLSTAT_QCHANGED</span><span class="sxs-lookup"><span data-stu-id="9de83-112">TBLSTAT_QCHANGED</span></span> 
  
> <span data-ttu-id="9de83-113">表の内容が expectantly 変更されました。</span><span class="sxs-lookup"><span data-stu-id="9de83-113">The contents of the table have expectantly changed.</span></span> <span data-ttu-id="9de83-114">この状態値は、並べ替えまたは制限の操作によって発生した変更に対しては返されません。</span><span class="sxs-lookup"><span data-stu-id="9de83-114">This status value is not returned for changes that result from sort or restriction operations.</span></span>
    
<span data-ttu-id="9de83-115">TBLSTAT_RESTRICT_ERROR</span><span class="sxs-lookup"><span data-stu-id="9de83-115">TBLSTAT_RESTRICT_ERROR</span></span> 
  
> <span data-ttu-id="9de83-116">[IMAPITable:: Restrict](imapitable-restrict.md)操作中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="9de83-116">An error occurred during an [IMAPITable::Restrict](imapitable-restrict.md) operation.</span></span> 
    
<span data-ttu-id="9de83-117">TBLSTAT_RESTRICTING</span><span class="sxs-lookup"><span data-stu-id="9de83-117">TBLSTAT_RESTRICTING</span></span> 
  
> <span data-ttu-id="9de83-118">**IMAPITable:: Restrict**操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="9de83-118">An **IMAPITable::Restrict** operation is in progress.</span></span> 
    
<span data-ttu-id="9de83-119">TBLSTAT_SETCOL_ERROR</span><span class="sxs-lookup"><span data-stu-id="9de83-119">TBLSTAT_SETCOL_ERROR</span></span> 
  
> <span data-ttu-id="9de83-120">[IMAPITable:: SetColumns](imapitable-setcolumns.md)操作中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="9de83-120">An error occurred during an [IMAPITable::SetColumns](imapitable-setcolumns.md) operation.</span></span> 
    
<span data-ttu-id="9de83-121">TBLSTAT_SETTING_COLS</span><span class="sxs-lookup"><span data-stu-id="9de83-121">TBLSTAT_SETTING_COLS</span></span> 
  
> <span data-ttu-id="9de83-122">**IMAPITable:: SetColumns**操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="9de83-122">An **IMAPITable::SetColumns** operation is in progress.</span></span> 
    
<span data-ttu-id="9de83-123">TBLSTAT_SORT_ERROR</span><span class="sxs-lookup"><span data-stu-id="9de83-123">TBLSTAT_SORT_ERROR</span></span> 
  
> <span data-ttu-id="9de83-124">[IMAPITable:: sorttable](imapitable-sorttable.md)操作中にエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="9de83-124">An error occurred during an [IMAPITable::SortTable](imapitable-sorttable.md) operation.</span></span> 
    
<span data-ttu-id="9de83-125">TBLSTAT_SORTING</span><span class="sxs-lookup"><span data-stu-id="9de83-125">TBLSTAT_SORTING</span></span> 
  
> <span data-ttu-id="9de83-126">**IMAPITable:: sorttable**操作が進行中です。</span><span class="sxs-lookup"><span data-stu-id="9de83-126">An **IMAPITable::SortTable** operation is in progress.</span></span> 
    
 <span data-ttu-id="9de83-127">_lpulTableType_</span><span class="sxs-lookup"><span data-stu-id="9de83-127">_lpulTableType_</span></span>
  
> <span data-ttu-id="9de83-128">読み上げテーブルの種類を示す値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="9de83-128">[out] Pointer to a value that indicates the table's type.</span></span> <span data-ttu-id="9de83-129">次の3種類のテーブルのいずれかを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="9de83-129">One of the following three table types can be returned:</span></span>
    
<span data-ttu-id="9de83-130">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="9de83-130">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="9de83-131">テーブルの内容は動的です。行と列の値は、基になるデータが変更されたときに変更されることがあります。</span><span class="sxs-lookup"><span data-stu-id="9de83-131">The table's contents are dynamic; the rows and column values can change as the underlying data changes.</span></span>
    
<span data-ttu-id="9de83-132">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="9de83-132">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="9de83-133">テーブル内の行は固定されていますが、これらの行の列の値は動的であり、基になるデータの変更として変更できます。</span><span class="sxs-lookup"><span data-stu-id="9de83-133">The rows within the table are fixed, but the values of the columns within these rows are dynamic and can change as the underlying data changes.</span></span>
    
<span data-ttu-id="9de83-134">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="9de83-134">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="9de83-135">テーブルは静的であり、基になるデータが変更されてもその内容は変更されません。</span><span class="sxs-lookup"><span data-stu-id="9de83-135">The table is static, and its contents do not change when the underlying data changes.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9de83-136">戻り値</span><span class="sxs-lookup"><span data-stu-id="9de83-136">Return value</span></span>

<span data-ttu-id="9de83-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="9de83-137">S_OK</span></span> 
  
> <span data-ttu-id="9de83-138">テーブルの状態が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="9de83-138">The table's status was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9de83-139">注釈</span><span class="sxs-lookup"><span data-stu-id="9de83-139">Remarks</span></span>

<span data-ttu-id="9de83-140">**IMAPTable:: GetStatus**メソッドは、テーブルの種類と現在の状態に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="9de83-140">The **IMAPTable::GetStatus** method retrieves information about a table's type and current status.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9de83-141">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="9de83-141">Notes to callers</span></span>

<span data-ttu-id="9de83-142">**GetStatus**を3つの他の**IMAPITable**メソッドと組み合わせて使用すると、これらの操作の状態を監視し、テーブルに対する効果を確認できます。</span><span class="sxs-lookup"><span data-stu-id="9de83-142">You can use **GetStatus** in conjunction with three other **IMAPITable** methods to monitor the status of those operations and determine the effect on the table.</span></span> <span data-ttu-id="9de83-143">次の**IMAPITable**呼び出しのいずれかを行った後、 **GetStatus**を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9de83-143">Call **GetStatus** after making one of the following **IMAPITable** calls:</span></span> 
  
- <span data-ttu-id="9de83-144">[IMAPITable::](imapitable-restrict.md)制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="9de83-144">[IMAPITable::Restrict](imapitable-restrict.md) to set a restriction.</span></span> 
    
- <span data-ttu-id="9de83-145">[IMAPITable:: sorttable](imapitable-sorttable.md)は、並べ替えの順序を設定します。</span><span class="sxs-lookup"><span data-stu-id="9de83-145">[IMAPITable::SortTable](imapitable-sorttable.md) to establish a sort order.</span></span> 
    
- <span data-ttu-id="9de83-146">[IMAPITable:: SetColumns](imapitable-setcolumns.md)列セットを定義します。</span><span class="sxs-lookup"><span data-stu-id="9de83-146">[IMAPITable::SetColumns](imapitable-setcolumns.md) to define a column set.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="9de83-147">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="9de83-147">MFCMAPI reference</span></span>

<span data-ttu-id="9de83-148">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9de83-148">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9de83-149">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="9de83-149">**File**</span></span>|<span data-ttu-id="9de83-150">**関数**</span><span class="sxs-lookup"><span data-stu-id="9de83-150">**Function**</span></span>|<span data-ttu-id="9de83-151">**コメント**</span><span class="sxs-lookup"><span data-stu-id="9de83-151">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9de83-152">ContentsTableListCtrl</span><span class="sxs-lookup"><span data-stu-id="9de83-152">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="9de83-153">CContentsTableListCtrl:: GetStatus</span><span class="sxs-lookup"><span data-stu-id="9de83-153">CContentsTableListCtrl::GetStatus</span></span>  <br/> |<span data-ttu-id="9de83-154">mfcmapi は、 **IMAPITable:: GetStatus**メソッドを使用して、テーブルの状態を報告します。</span><span class="sxs-lookup"><span data-stu-id="9de83-154">MFCMAPI uses the **IMAPITable::GetStatus** method to report the status of a table.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9de83-155">関連項目</span><span class="sxs-lookup"><span data-stu-id="9de83-155">See also</span></span>



[<span data-ttu-id="9de83-156">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="9de83-156">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="9de83-157">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="9de83-157">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="9de83-158">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="9de83-158">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="9de83-159">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9de83-159">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="9de83-160">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="9de83-160">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

