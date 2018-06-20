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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b14529e987b85d1dcbe3689d4e852a9efd39a396
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801664"
---
# <a name="notifcallback"></a><span data-ttu-id="3ef54-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="3ef54-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="3ef54-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3ef54-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3ef54-105">MAPI 呼び出しをイベント通知を送信するコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="3ef54-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="3ef54-106">このコールバック関数は、 [HrAllocAdviseSink](hrallocadvisesink.md)関数を呼び出すことによって作成されたアドバイズ シンク オブジェクトにラップするときにのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="3ef54-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3ef54-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="3ef54-107">Header file:</span></span>  <br/> |<span data-ttu-id="3ef54-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3ef54-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3ef54-109">によって実装される関数の定義:</span><span class="sxs-lookup"><span data-stu-id="3ef54-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="3ef54-110">クライアント アプリケーションとサービス ・ プロバイダー</span><span class="sxs-lookup"><span data-stu-id="3ef54-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="3ef54-111">によって呼び出される関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="3ef54-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="3ef54-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="3ef54-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="3ef54-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="3ef54-113">Parameters</span></span>

 <span data-ttu-id="3ef54-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="3ef54-114">_lpvContext_</span></span>
  
> <span data-ttu-id="3ef54-115">[in]任意の値へのポインターは、MAPI では、それを呼び出すときに、コールバック関数に渡されます。</span><span class="sxs-lookup"><span data-stu-id="3ef54-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="3ef54-116">この値は重要では、クライアント アプリケーションまたはサービス プロバイダーにアドレスを表すことができます。</span><span class="sxs-lookup"><span data-stu-id="3ef54-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="3ef54-117">通常、C++ コードでは、 _lpvContext_パラメーターのポインターを表します C++ オブジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="3ef54-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="3ef54-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="3ef54-118">_cNotification_</span></span>
  
> <span data-ttu-id="3ef54-119">[in]_LpNotifications_パラメーターで指定された配列内のイベント通知の数です。</span><span class="sxs-lookup"><span data-stu-id="3ef54-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="3ef54-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="3ef54-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="3ef54-121">[out]この関数が書き込む場所[通知](notification.md)の構造体の配列をバッファーへのポインターには、イベント通知が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3ef54-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3ef54-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3ef54-122">Return value</span></span>

<span data-ttu-id="3ef54-123">**NOTIFCALLBACK**関数のプロトタイプ用の有効な戻り値のセットは、クライアント アプリケーションまたはサービス プロバイダーでこの関数を実装するかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="3ef54-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="3ef54-124">クライアントは、S_OK を返す常にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3ef54-124">Clients should always return S_OK.</span></span> <span data-ttu-id="3ef54-125">プロバイダーには、S_OK または CALLBACK_DISCONTINUE のいずれかを返すことができます。</span><span class="sxs-lookup"><span data-stu-id="3ef54-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3ef54-126">備考</span><span class="sxs-lookup"><span data-stu-id="3ef54-126">Remarks</span></span>

<span data-ttu-id="3ef54-127">CALLBACK_DISCONTINUE は、有効な戻り値の同期のコールバック関数だけです。MAPI すぐに停止するこの通知のコールバックの処理を要求します。</span><span class="sxs-lookup"><span data-stu-id="3ef54-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="3ef54-128">CALLBACK_DISCONTINUE が返された場合は、MAPI は[IMAPISupport::Notify](imapisupport-notify.md)すると、NOTIFY_CANCELED に_lpUlFlags_パラメーターを設定します。</span><span class="sxs-lookup"><span data-stu-id="3ef54-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="3ef54-129">同期コールバック関数の機能に制約は、次のように。</span><span class="sxs-lookup"><span data-stu-id="3ef54-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="3ef54-130">これが原因で、別の同期通知を生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="3ef54-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="3ef54-131">ユーザー インターフェイスを表示することはできません。</span><span class="sxs-lookup"><span data-stu-id="3ef54-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3ef54-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="3ef54-132">See also</span></span>



[<span data-ttu-id="3ef54-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="3ef54-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

