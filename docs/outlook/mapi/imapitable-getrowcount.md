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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425604"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="f1f6b-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="f1f6b-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="f1f6b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1f6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f1f6b-105">テーブル内の行の総数を返します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="f1f6b-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f1f6b-106">Parameters</span></span>

 <span data-ttu-id="f1f6b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f1f6b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f1f6b-108">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f1f6b-109">_lpulCount_</span><span class="sxs-lookup"><span data-stu-id="f1f6b-109">_lpulCount_</span></span>
  
> <span data-ttu-id="f1f6b-110">[out]テーブル内の行数へのポインター。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f1f6b-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="f1f6b-111">Return value</span></span>

<span data-ttu-id="f1f6b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="f1f6b-112">S_OK</span></span> 
  
> <span data-ttu-id="f1f6b-113">行数が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="f1f6b-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f1f6b-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f1f6b-115">別の操作が進行中で、行数の取得操作が開始されません。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="f1f6b-116">進行中の操作の完了を許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="f1f6b-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f1f6b-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="f1f6b-118">テーブルは行数を計算できません。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="f1f6b-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="f1f6b-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="f1f6b-120">呼び出しは成功しましたが、メモリの制約により正確な行数を決定できない可能性が高いので、おおよその行数が返されました。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="f1f6b-121">この警告をテストするには、次のマクロ **HR_FAILED** します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="f1f6b-122">「エラー [処理のためのマクロの使用」を参照してください](using-macros-for-error-handling.md)。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f1f6b-123">注釈</span><span class="sxs-lookup"><span data-stu-id="f1f6b-123">Remarks</span></span>

<span data-ttu-id="f1f6b-124">**IMAPITable::GetRowCount** メソッドは、テーブル内の行の総数を取得します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f1f6b-125">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="f1f6b-125">Notes to implementers</span></span>

<span data-ttu-id="f1f6b-126">テーブルの正確な行数を確認できない場合は  _、lpulCount_ パラメーター MAPI_W_APPROX_COUNTの値と近似行数を返します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f1f6b-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="f1f6b-127">Notes to callers</span></span>

<span data-ttu-id="f1f6b-128">**GetRowCount を使用** して、データを取得するために [IMAPITable::QueryRows](imapitable-queryrows.md)メソッドを呼び出す前に、テーブルが保持する行の数を確認します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="f1f6b-129">テーブルに 20 行未満の行がある場合は **、QueryPosition** を呼び出してテーブル全体を取得しても安全です。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="f1f6b-130">テーブル内に 20 行を超える行がある場合は **、QueryPosition** に対して複数の呼び出しを行い、各呼び出しで取得される行数を制限します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="f1f6b-131">一部のテーブルは **GetRowCount をサポートしていないの** で、この値MAPI_E_NO_SUPPORT。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="f1f6b-132">**GetRowCount が** サポートされていない場合は [、IMAPITable::QueryPosition](imapitable-queryposition.md)を呼び出す方法があります。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="f1f6b-133">QueryPosition の結果 **を使用** して、現在の行と最後の行の関係を決定できます。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="f1f6b-134">**GetRowCount** が一MAPI_E_BUSY行数を取得することができないため、この値を返す場合は [、IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="f1f6b-135">**WaitForCompletion が返** された場合は **、GetRowCount の呼び出しを再試行します**。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="f1f6b-136">非同期操作が進行中かどうかを検出するもう 1 つの方法は [、IMAPITable::GetStatus](imapitable-getstatus.md) メソッドを呼び出し  _、lpulTableState_ パラメーターの内容を確認する方法です。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f1f6b-137">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="f1f6b-137">MFCMAPI reference</span></span>

<span data-ttu-id="f1f6b-138">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f1f6b-139">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="f1f6b-139">**File**</span></span>|<span data-ttu-id="f1f6b-140">**関数**</span><span class="sxs-lookup"><span data-stu-id="f1f6b-140">**Function**</span></span>|<span data-ttu-id="f1f6b-141">**コメント**</span><span class="sxs-lookup"><span data-stu-id="f1f6b-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f1f6b-142">MAPIFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="f1f6b-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="f1f6b-143">CopyFolderContents</span><span class="sxs-lookup"><span data-stu-id="f1f6b-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="f1f6b-144">MFCMAPI は **IMAPITable::GetRowCount** メソッドを使用して、コピーを実行するためにメモリを割り当て可能なソース テーブル内の行数を決定します。</span><span class="sxs-lookup"><span data-stu-id="f1f6b-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1f6b-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="f1f6b-145">See also</span></span>



[<span data-ttu-id="f1f6b-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="f1f6b-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="f1f6b-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="f1f6b-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="f1f6b-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="f1f6b-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="f1f6b-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="f1f6b-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="f1f6b-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f1f6b-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="f1f6b-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="f1f6b-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

