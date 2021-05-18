---
title: IMAPITableWaitForCompletion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.WaitForCompletion
api_type:
- COM
ms.assetid: 7663c640-396e-4720-9345-370d0856bd49
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 778ff8f36478740e5ee23ba439db1e328eca2e06
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407061"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="6c3dd-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="6c3dd-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="6c3dd-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c3dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c3dd-105">テーブルで進行中の 1 つ以上の非同期操作が完了するまで、処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="6c3dd-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6c3dd-106">Parameters</span></span>

 <span data-ttu-id="6c3dd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6c3dd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6c3dd-108">予約済み。は 0 である必要があります。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6c3dd-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="6c3dd-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="6c3dd-110">[in]非同期操作または操作が完了するまで待機する最大ミリ秒数。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="6c3dd-111">完了するまで無期限に待機するには  _、ulTimeout_ を 0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="6c3dd-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="6c3dd-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="6c3dd-113">[in, out]入力時に、有効なポインターまたは NULL のいずれか。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="6c3dd-114">出力時に  _、lpulTableStatus_ が有効なポインターである場合は、表の最新の状態を指します。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="6c3dd-115">_lpulTableStatus が_ NULL の場合、状態情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="6c3dd-116">**WaitForCompletion が** 失敗した HRESULT 値を返す場合 _、lpulTableStatus_ の内容は未定義です。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6c3dd-117">戻り値</span><span class="sxs-lookup"><span data-stu-id="6c3dd-117">Return value</span></span>

<span data-ttu-id="6c3dd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="6c3dd-118">S_OK</span></span> 
  
> <span data-ttu-id="6c3dd-119">待機操作が成功しました。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="6c3dd-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6c3dd-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="6c3dd-121">この表では、非同期操作の完了を待機する機能はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="6c3dd-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="6c3dd-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="6c3dd-123">指定された時間内に非同期操作または操作が完了しなかった。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c3dd-124">注釈</span><span class="sxs-lookup"><span data-stu-id="6c3dd-124">Remarks</span></span>

<span data-ttu-id="6c3dd-125">**IMAPITable::WaitForCompletion** メソッドは、テーブルの現在進行中の非同期操作が完了するまで処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="6c3dd-126">**WaitForCompletion** を使用すると、非同期操作を完全に完了するか  _、ulTimeout_ で示されているミリ秒単位で実行してから中断することができます。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="6c3dd-127">進行中の非同期操作を検出するには [、IMAPITable::GetStatus メソッドを呼び出](imapitable-getstatus.md) します。</span><span class="sxs-lookup"><span data-stu-id="6c3dd-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c3dd-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="6c3dd-128">See also</span></span>



[<span data-ttu-id="6c3dd-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="6c3dd-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="6c3dd-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="6c3dd-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="6c3dd-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="6c3dd-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="6c3dd-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="6c3dd-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="6c3dd-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="6c3dd-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="6c3dd-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6c3dd-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

