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
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c7859e033924786e415f9faa9f75021ea47968c6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800854"
---
# <a name="imapitablewaitforcompletion"></a><span data-ttu-id="3f5af-103">IMAPITable::WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="3f5af-103">IMAPITable::WaitForCompletion</span></span>

  
  
<span data-ttu-id="3f5af-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f5af-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f5af-105">1 つまたは複数の非同期操作の進行状況でテーブルに完了するまでの処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="3f5af-105">Suspends processing until one or more asynchronous operations in progress on the table have completed.</span></span>
  
```cpp
HRESULT WaitForCompletion(
ULONG ulFlags,
ULONG ulTimeout,
ULONG FAR * lpulTableStatus
);
```

## <a name="parameters"></a><span data-ttu-id="3f5af-106">�p�����[�^�[</span><span class="sxs-lookup"><span data-stu-id="3f5af-106">Parameters</span></span>

 <span data-ttu-id="3f5af-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3f5af-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3f5af-108">予約されています。0 にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3f5af-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="3f5af-109">_ulTimeout_</span><span class="sxs-lookup"><span data-stu-id="3f5af-109">_ulTimeout_</span></span>
  
> <span data-ttu-id="3f5af-110">[in]非同期操作または操作が完了するまで待機するミリ秒単位の最大数。</span><span class="sxs-lookup"><span data-stu-id="3f5af-110">[in] Maximum number of milliseconds to wait for the asynchronous operation or operations to complete.</span></span> <span data-ttu-id="3f5af-111">完了が発生するまで無期限に待機するには、 _ulTimeout_を 0 xffffffff に設定します。</span><span class="sxs-lookup"><span data-stu-id="3f5af-111">To wait indefinitely until completion occurs, set  _ulTimeout_ to 0xFFFFFFFF.</span></span> 
    
 <span data-ttu-id="3f5af-112">_lpulTableStatus_</span><span class="sxs-lookup"><span data-stu-id="3f5af-112">_lpulTableStatus_</span></span>
  
> <span data-ttu-id="3f5af-113">[で [チェック アウト]有効なポインターまたは NULL のいずれかは、入力します。</span><span class="sxs-lookup"><span data-stu-id="3f5af-113">[in, out] On input, either a valid pointer or NULL.</span></span> <span data-ttu-id="3f5af-114">出力では、 _lpulTableStatus_が有効なポインターである場合、ポイント テーブルの最新の状態にします。</span><span class="sxs-lookup"><span data-stu-id="3f5af-114">On output, if  _lpulTableStatus_ is a valid pointer, it points to the most recent status of the table.</span></span> <span data-ttu-id="3f5af-115">_LpulTableStatus_が NULL の場合は、ステータス情報は返されません。</span><span class="sxs-lookup"><span data-stu-id="3f5af-115">If  _lpulTableStatus_ is NULL, no status information is returned.</span></span> <span data-ttu-id="3f5af-116">**WaitForCompletion**失敗の HRESULT 値が返された場合の_lpulTableStatus_の内容は定義されていません。</span><span class="sxs-lookup"><span data-stu-id="3f5af-116">If **WaitForCompletion** returns an unsuccessful HRESULT value, the contents of  _lpulTableStatus_ are undefined.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3f5af-117">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3f5af-117">Return value</span></span>

<span data-ttu-id="3f5af-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3f5af-118">S_OK</span></span> 
  
> <span data-ttu-id="3f5af-119">待ち操作が正常に完了しました。</span><span class="sxs-lookup"><span data-stu-id="3f5af-119">The wait operation was successful.</span></span>
    
<span data-ttu-id="3f5af-120">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3f5af-120">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3f5af-121">テーブルは、非同期操作の完了の待機をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3f5af-121">The table does not support waiting for the completion of asynchronous operations.</span></span>
    
<span data-ttu-id="3f5af-122">MAPI_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="3f5af-122">MAPI_E_TIMEOUT</span></span> 
  
> <span data-ttu-id="3f5af-123">非同期操作または操作は、指定した時間に完了しませんでした。</span><span class="sxs-lookup"><span data-stu-id="3f5af-123">The asynchronous operation or operations did not complete in the specified time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3f5af-124">備考</span><span class="sxs-lookup"><span data-stu-id="3f5af-124">Remarks</span></span>

<span data-ttu-id="3f5af-125">**IMAPITable::WaitForCompletion**メソッドは、テーブルのため現在の非同期操作が完了するまでの処理を中断します。</span><span class="sxs-lookup"><span data-stu-id="3f5af-125">The **IMAPITable::WaitForCompletion** method suspends processing until any asynchronous operations currently under way for the table have completed.</span></span> <span data-ttu-id="3f5af-126">**WaitForCompletion**ことができます、非同期操作のいずれか完全に完了または中断される前に、 _ulTimeout_で示されたミリ秒数を実行します。</span><span class="sxs-lookup"><span data-stu-id="3f5af-126">**WaitForCompletion** can allow the asynchronous operations either to fully complete or to run for a certain number of milliseconds, as indicated by  _ulTimeout_, before being interrupted.</span></span> <span data-ttu-id="3f5af-127">進行中の非同期操作を検出するためには、 [IMAPITable::GetStatus](imapitable-getstatus.md)メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="3f5af-127">To detect asynchronous operations in progress, call the [IMAPITable::GetStatus](imapitable-getstatus.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f5af-128">関連項目</span><span class="sxs-lookup"><span data-stu-id="3f5af-128">See also</span></span>



[<span data-ttu-id="3f5af-129">IMAPITable::GetRowCount</span><span class="sxs-lookup"><span data-stu-id="3f5af-129">IMAPITable::GetRowCount</span></span>](imapitable-getrowcount.md)
  
[<span data-ttu-id="3f5af-130">IMAPITable::GetStatus</span><span class="sxs-lookup"><span data-stu-id="3f5af-130">IMAPITable::GetStatus</span></span>](imapitable-getstatus.md)
  
[<span data-ttu-id="3f5af-131">IMAPITable::Restrict</span><span class="sxs-lookup"><span data-stu-id="3f5af-131">IMAPITable::Restrict</span></span>](imapitable-restrict.md)
  
[<span data-ttu-id="3f5af-132">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="3f5af-132">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="3f5af-133">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="3f5af-133">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="3f5af-134">IMAPITable: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f5af-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

