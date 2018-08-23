---
title: IMAPITableGetRowCount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetRowCount
api_type:
- COM
ms.assetid: 44a12c92-7462-4acf-9520-5d4c2d7f1d47
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 71178f1a531bd381387e0aa7fbacb02d4431a401
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584325"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="4122a-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="4122a-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="4122a-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4122a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4122a-105">テーブル内の行の合計数を返します。</span><span class="sxs-lookup"><span data-stu-id="4122a-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="4122a-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="4122a-106">Parameters</span></span>

 <span data-ttu-id="4122a-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4122a-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4122a-108">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4122a-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="4122a-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="4122a-109">_lpulCount_</span></span>
  
> <span data-ttu-id="4122a-110">[out]テーブル内の行の数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="4122a-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4122a-111">�߂�l</span><span class="sxs-lookup"><span data-stu-id="4122a-111">Return value</span></span>

<span data-ttu-id="4122a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="4122a-112">S_OK</span></span> 
  
> <span data-ttu-id="4122a-113">ローの数が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="4122a-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="4122a-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4122a-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4122a-115">別の操作は、行カウントの取得操作の開始を防止する処理中です。</span><span class="sxs-lookup"><span data-stu-id="4122a-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="4122a-116">実行中の操作を完了できるか、それを停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4122a-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="4122a-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="4122a-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="4122a-118">テーブルは、行の数を計算できません。</span><span class="sxs-lookup"><span data-stu-id="4122a-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="4122a-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="4122a-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="4122a-120">呼び出しが成功したが、行数の正確な判断できませんでした可能性のあるメモリの制約があるために、おおよその行数が返されました。</span><span class="sxs-lookup"><span data-stu-id="4122a-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="4122a-121">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="4122a-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="4122a-122">[エラー処理のためのマクロを使用する](using-macros-for-error-handling.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4122a-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4122a-123">注釈</span><span class="sxs-lookup"><span data-stu-id="4122a-123">Remarks</span></span>

<span data-ttu-id="4122a-124">**IMAPITable::GetRowCount**メソッドは、テーブル内の行の合計数を取得します。</span><span class="sxs-lookup"><span data-stu-id="4122a-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4122a-125">実装者へのメモ</span><span class="sxs-lookup"><span data-stu-id="4122a-125">Notes to implementers</span></span>

<span data-ttu-id="4122a-126">テーブルの正確な行数を判断できない、戻り値の MAPI_W_APPROX_COUNT と、おおよその行が、 _lpulCount_パラメーターの内容をカウントします。</span><span class="sxs-lookup"><span data-stu-id="4122a-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4122a-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="4122a-127">Notes to callers</span></span>

<span data-ttu-id="4122a-128">データを取得するために、 [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドの呼び出しを行う前にテーブルの行の数を検索する使用**な**を保持します。</span><span class="sxs-lookup"><span data-stu-id="4122a-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="4122a-129">テーブルに 20 未満の行がある場合は、テーブル全体を取得するために**QueryPosition**を呼び出しても安全です。</span><span class="sxs-lookup"><span data-stu-id="4122a-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="4122a-130">テーブルに 20 を超える行がある場合は、 **QueryPosition**を複数回呼び出すことを検討してくださいし、呼び出しのたびに取得される行の数を制限します。</span><span class="sxs-lookup"><span data-stu-id="4122a-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="4122a-131">いくつかのテーブルをサポートしない**な**MAPI_E_NO_SUPPORT を取得します。</span><span class="sxs-lookup"><span data-stu-id="4122a-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="4122a-132">**な**はサポートされていない場合、 [IMAPITable::QueryPosition](imapitable-queryposition.md)を呼び出す別の方法を引き起こすことがあります。</span><span class="sxs-lookup"><span data-stu-id="4122a-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="4122a-133">**QueryPosition**から結果には、現在の行と最後の行の間の関係を指定できます。</span><span class="sxs-lookup"><span data-stu-id="4122a-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="4122a-134">**な**に MAPI_E_BUSY が返されるは、行の数を取得するために一時的にできないため、ときに、 [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="4122a-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="4122a-135">**WaitForCompletion**が返されるときは、**な**への呼び出しを再試行します。</span><span class="sxs-lookup"><span data-stu-id="4122a-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="4122a-136">非同期操作が進行中かどうかを検出するために別の方法では、 [IMAPITable::GetStatus](imapitable-getstatus.md)メソッドを呼び出すし、 _lpulTableState_パラメーターの内容を確認します。</span><span class="sxs-lookup"><span data-stu-id="4122a-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4122a-137">MFCMAPI 参照</span><span class="sxs-lookup"><span data-stu-id="4122a-137">MFCMAPI reference</span></span>

<span data-ttu-id="4122a-138">MFCMAPI �T���v�� �R�[�h�ł́A���̕\��Q�Ƃ��Ă��������B</span><span class="sxs-lookup"><span data-stu-id="4122a-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4122a-139">**�t�@�C��**</span><span class="sxs-lookup"><span data-stu-id="4122a-139">**File**</span></span>|<span data-ttu-id="4122a-140">**�֐�**</span><span class="sxs-lookup"><span data-stu-id="4122a-140">**Function**</span></span>|<span data-ttu-id="4122a-141">**�R�����g**</span><span class="sxs-lookup"><span data-stu-id="4122a-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4122a-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="4122a-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="4122a-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="4122a-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="4122a-144">MFCMAPI では、 **IMAPITable::GetRowCount**メソッドを使用して、コピーを実行するのにはメモリの割り当てができるように、ソース テーブルでは、行の数を決定します。</span><span class="sxs-lookup"><span data-stu-id="4122a-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4122a-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="4122a-145">See also</span></span>



[<span data-ttu-id="4122a-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="4122a-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="4122a-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="4122a-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="4122a-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="4122a-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="4122a-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="4122a-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="4122a-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4122a-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="4122a-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="4122a-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

