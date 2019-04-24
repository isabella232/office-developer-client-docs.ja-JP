---
title: NOTIFCALLBACK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.NOTIFCALLBACK
api_type:
- COM
ms.assetid: 416008b4-13aa-4387-8c12-f8f2ca252391
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334476"
---
# <a name="notifcallback"></a><span data-ttu-id="2ee86-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="2ee86-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="2ee86-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ee86-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ee86-105">イベント通知を送信するために MAPI が呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="2ee86-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="2ee86-106">このコールバック関数は、 [HrAllocAdviseSink](hrallocadvisesink.md)関数を呼び出すことによって作成されたアドバイズシンクオブジェクトでラップされている場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="2ee86-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2ee86-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="2ee86-107">Header file:</span></span>  <br/> |<span data-ttu-id="2ee86-108">mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="2ee86-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="2ee86-109">定義された関数の実装:</span><span class="sxs-lookup"><span data-stu-id="2ee86-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="2ee86-110">クライアントアプリケーションとサービスプロバイダー</span><span class="sxs-lookup"><span data-stu-id="2ee86-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="2ee86-111">によって呼び出された定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="2ee86-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="2ee86-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="2ee86-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="2ee86-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2ee86-113">Parameters</span></span>

 <span data-ttu-id="2ee86-114">_lpvcontext_</span><span class="sxs-lookup"><span data-stu-id="2ee86-114">_lpvContext_</span></span>
  
> <span data-ttu-id="2ee86-115">順番MAPI がコールバック関数に渡す任意の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ee86-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="2ee86-116">この値は、クライアントアプリケーションまたはサービスプロバイダーにとって重要なアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="2ee86-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="2ee86-117">通常、c++ コードの場合、 _lpvcontext_パラメーターは c++ オブジェクトへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="2ee86-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="2ee86-118">_cnotification_</span><span class="sxs-lookup"><span data-stu-id="2ee86-118">_cNotification_</span></span>
  
> <span data-ttu-id="2ee86-119">順番lpnotifications パラメーターで指定された、配列__ 内のイベント通知の数。</span><span class="sxs-lookup"><span data-stu-id="2ee86-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="2ee86-120">_lpnotifications_</span><span class="sxs-lookup"><span data-stu-id="2ee86-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="2ee86-121">読み上げこの関数がイベント通知を含む[通知](notification.md)構造の配列を書き込む場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="2ee86-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2ee86-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="2ee86-122">Return value</span></span>

<span data-ttu-id="2ee86-123">**NOTIFCALLBACK**関数プロトタイプに対して有効な戻り値のセットは、関数がクライアントアプリケーションまたはサービスプロバイダーで実装されているかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2ee86-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="2ee86-124">クライアントは常に S_OK を返します。</span><span class="sxs-lookup"><span data-stu-id="2ee86-124">Clients should always return S_OK.</span></span> <span data-ttu-id="2ee86-125">プロバイダーは、S_OK または CALLBACK_DISCONTINUE のいずれかを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="2ee86-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2ee86-126">解説</span><span class="sxs-lookup"><span data-stu-id="2ee86-126">Remarks</span></span>

<span data-ttu-id="2ee86-127">CALLBACK_DISCONTINUE は、同期コールバック関数に対してのみ有効な戻り値です。この通知のコールバックの処理を直ちに停止するように MAPI に要求します。</span><span class="sxs-lookup"><span data-stu-id="2ee86-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="2ee86-128">CALLBACK_DISCONTINUE が返されると、MAPI は[imapisupport:: NOTIFY](imapisupport-notify.md)から戻るときに_lNOTIFY_CANCELED flags_パラメーターをに設定します。</span><span class="sxs-lookup"><span data-stu-id="2ee86-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="2ee86-129">以下に、同期コールバック関数で可能な処理に関する制限を示します。</span><span class="sxs-lookup"><span data-stu-id="2ee86-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="2ee86-130">別の同期通知が生成されることはありません。</span><span class="sxs-lookup"><span data-stu-id="2ee86-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="2ee86-131">ユーザーインターフェイスを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="2ee86-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2ee86-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="2ee86-132">See also</span></span>



[<span data-ttu-id="2ee86-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="2ee86-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

