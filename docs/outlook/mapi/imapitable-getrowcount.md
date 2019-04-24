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
ms.openlocfilehash: b13bf3bdd8392efc42ad189e48dffad8636f0708
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328890"
---
# <a name="imapitablegetrowcount"></a><span data-ttu-id="99f17-103">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="99f17-103">IMAPITable::GetRowCount</span></span>

  
  
<span data-ttu-id="99f17-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99f17-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99f17-105">テーブル内の行の総数を返します。</span><span class="sxs-lookup"><span data-stu-id="99f17-105">Returns the total number of rows in the table.</span></span> 
  
```cpp
HRESULT GetRowCount(
ULONG ulFlags,
ULONG FAR * lpulCount
);
```

## <a name="parameters"></a><span data-ttu-id="99f17-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="99f17-106">Parameters</span></span>

 <span data-ttu-id="99f17-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99f17-107">_ulFlags_</span></span>
  
> <span data-ttu-id="99f17-108">予約語0である必要があります。</span><span class="sxs-lookup"><span data-stu-id="99f17-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="99f17-109">_lルー count_</span><span class="sxs-lookup"><span data-stu-id="99f17-109">_lpulCount_</span></span>
  
> <span data-ttu-id="99f17-110">読み上げ表の行数へのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="99f17-110">[out] Pointer to the number of rows in the table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99f17-111">戻り値</span><span class="sxs-lookup"><span data-stu-id="99f17-111">Return value</span></span>

<span data-ttu-id="99f17-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="99f17-112">S_OK</span></span> 
  
> <span data-ttu-id="99f17-113">行数が正常に返されました。</span><span class="sxs-lookup"><span data-stu-id="99f17-113">The row count was successfully returned.</span></span>
    
<span data-ttu-id="99f17-114">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="99f17-114">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="99f17-115">別の操作が進行中であるため、行カウントの取得操作を開始できません。</span><span class="sxs-lookup"><span data-stu-id="99f17-115">Another operation is in progress that prevents the row count retrieval operation from starting.</span></span> <span data-ttu-id="99f17-116">進行中の操作が完了することを許可するか、停止する必要があります。</span><span class="sxs-lookup"><span data-stu-id="99f17-116">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="99f17-117">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="99f17-117">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="99f17-118">テーブルで行数を計算できません。</span><span class="sxs-lookup"><span data-stu-id="99f17-118">The table cannot calculate the number of rows.</span></span>
    
<span data-ttu-id="99f17-119">MAPI_W_APPROX_COUNT</span><span class="sxs-lookup"><span data-stu-id="99f17-119">MAPI_W_APPROX_COUNT</span></span> 
  
> <span data-ttu-id="99f17-120">呼び出しは成功しましたが、メモリの制約によって正確な行の数を特定できなかったため、おおよその行数が返されました。</span><span class="sxs-lookup"><span data-stu-id="99f17-120">The call succeeded, but an approximate row count was returned because the exact row count could not be determined possibly due to memory constraints.</span></span> <span data-ttu-id="99f17-121">この警告をテストするには、 **HR_FAILED**マクロを使用します。</span><span class="sxs-lookup"><span data-stu-id="99f17-121">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="99f17-122">「[エラー処理にマクロを使用する](using-macros-for-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99f17-122">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99f17-123">解説</span><span class="sxs-lookup"><span data-stu-id="99f17-123">Remarks</span></span>

<span data-ttu-id="99f17-124">**IMAPITable:: getrowcount**メソッドは、テーブル内の行の合計数を取得します。</span><span class="sxs-lookup"><span data-stu-id="99f17-124">The **IMAPITable::GetRowCount** method retrieves the total number of rows in a table.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="99f17-125">実装に関するメモ</span><span class="sxs-lookup"><span data-stu-id="99f17-125">Notes to implementers</span></span>

<span data-ttu-id="99f17-126">テーブルの正確な行数を特定できない場合は、 _lMAPI_W_APPROX_COUNT count_パラメーターの内容で、および近似値の行数を返します。</span><span class="sxs-lookup"><span data-stu-id="99f17-126">If you cannot determine the table's exact row count, return MAPI_W_APPROX_COUNT and an approximate row count in the contents of the  _lpulCount_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99f17-127">呼び出し側への注意</span><span class="sxs-lookup"><span data-stu-id="99f17-127">Notes to callers</span></span>

<span data-ttu-id="99f17-128">データを取得するために[IMAPITable:: QueryRows](imapitable-queryrows.md)メソッドを呼び出す前に、 **getrowcount**を使用して、テーブルに保持されている行の数を調べます。</span><span class="sxs-lookup"><span data-stu-id="99f17-128">Use **GetRowCount** to find out how many rows a table holds before making a call to the [IMAPITable::QueryRows](imapitable-queryrows.md) method to retrieve the data.</span></span> <span data-ttu-id="99f17-129">テーブルに20行未満の行がある場合は、 **queryposition**を呼び出してテーブル全体を取得するのが安全です。</span><span class="sxs-lookup"><span data-stu-id="99f17-129">If there are less than twenty rows in the table, it is safe to call **QueryPosition** to retrieve the whole table.</span></span> <span data-ttu-id="99f17-130">テーブルに20行を超える行がある場合は、複数の呼び出しを**queryposition**に設定し、呼び出しごとに取得する行数を制限することを検討してください。</span><span class="sxs-lookup"><span data-stu-id="99f17-130">If there are more than twenty rows in the table, consider making multiple calls to **QueryPosition** and limit the number of rows retrieved in each call.</span></span> 
  
<span data-ttu-id="99f17-131">一部のテーブルは、 **getrowcount**をサポートせず、MAPI_E_NO_SUPPORT を返します。</span><span class="sxs-lookup"><span data-stu-id="99f17-131">Some tables do not support **GetRowCount** and return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="99f17-132">**getrowcount**がサポートされていない場合、次の方法で[IMAPITable:: queryposition](imapitable-queryposition.md)を呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="99f17-132">If **GetRowCount** is not supported, an alternative might be to call [IMAPITable::QueryPosition](imapitable-queryposition.md).</span></span> <span data-ttu-id="99f17-133">**queryposition**からの結果を使用して、現在の行と最後の行の間の関係を判断できます。</span><span class="sxs-lookup"><span data-stu-id="99f17-133">With the results from **QueryPosition**, you can determine the relationship between the current row and last row.</span></span> 
  
<span data-ttu-id="99f17-134">一時的に行数を取得できないために**getrowcount**が MAPI_E_BUSY を返す場合は、 [IMAPITable:: waitforcompletion](imapitable-waitforcompletion.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="99f17-134">When **GetRowCount** returns MAPI_E_BUSY because it is temporarily unable to retrieve a row count, call the [IMAPITable::WaitForCompletion](imapitable-waitforcompletion.md) method.</span></span> <span data-ttu-id="99f17-135">**waitforcompletion**が戻るときに、 **getrowcount**への呼び出しを再試行します。</span><span class="sxs-lookup"><span data-stu-id="99f17-135">When **WaitForCompletion** returns, retry the call to **GetRowCount**.</span></span> <span data-ttu-id="99f17-136">非同期操作が進行中かどうかを検出する別の方法として、 [IMAPITable:: GetStatus](imapitable-getstatus.md)メソッドを呼び出し、 _lpultablestate_パラメーターの内容を確認する方法があります。</span><span class="sxs-lookup"><span data-stu-id="99f17-136">Another way to detect whether an asynchronous operation is in progress is to call the [IMAPITable::GetStatus](imapitable-getstatus.md) method and check the contents of the  _lpulTableState_ parameter.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="99f17-137">MFCMAPI リファレンス</span><span class="sxs-lookup"><span data-stu-id="99f17-137">MFCMAPI reference</span></span>

<span data-ttu-id="99f17-138">MFCMAPI のサンプル コードについては、次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="99f17-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="99f17-139">**ファイル**</span><span class="sxs-lookup"><span data-stu-id="99f17-139">**File**</span></span>|<span data-ttu-id="99f17-140">**関数**</span><span class="sxs-lookup"><span data-stu-id="99f17-140">**Function**</span></span>|<span data-ttu-id="99f17-141">**コメント**</span><span class="sxs-lookup"><span data-stu-id="99f17-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99f17-142">MAPIFunctions</span><span class="sxs-lookup"><span data-stu-id="99f17-142">MAPIFunctions.cpp</span></span>  <br/> |<span data-ttu-id="99f17-143">copyfoldercontents</span><span class="sxs-lookup"><span data-stu-id="99f17-143">CopyFolderContents</span></span>  <br/> |<span data-ttu-id="99f17-144">mfcmapi は、 **IMAPITable:: getrowcount**メソッドを使用して、ソーステーブルにある行数を調べて、コピーを実行するためのメモリを割り当てることができるようにします。</span><span class="sxs-lookup"><span data-stu-id="99f17-144">MFCMAPI uses the **IMAPITable::GetRowCount** method to determine how many rows are in the source table so memory can be allocated to perform the copy.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="99f17-145">関連項目</span><span class="sxs-lookup"><span data-stu-id="99f17-145">See also</span></span>



[<span data-ttu-id="99f17-146">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="99f17-146">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="99f17-147">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="99f17-147">IMAPITable::QueryPosition</span></span>](imapitable-queryposition.md)
  
[<span data-ttu-id="99f17-148">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="99f17-148">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="99f17-149">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="99f17-149">IMAPITable::WaitForCompletion</span></span>](imapitable-waitforcompletion.md)
  
[<span data-ttu-id="99f17-150">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99f17-150">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


<span data-ttu-id="99f17-151">[�R�[�h �T���v���Ƃ��� MFCMAPI](mfcmapi-as-a-code-sample.md)</span><span class="sxs-lookup"><span data-stu-id="99f17-151">[MFCMAPI as a Code Sample](mfcmapi-as-a-code-sample.md)</span></span>

