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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 0e2a1a582894e082722d73422fc8bafe34c4230c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434019"
---
# <a name="notifcallback"></a><span data-ttu-id="20e66-103">NOTIFCALLBACK</span><span class="sxs-lookup"><span data-stu-id="20e66-103">NOTIFCALLBACK</span></span>

  
  
<span data-ttu-id="20e66-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20e66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20e66-105">MAPI がイベント通知を送信するために呼び出すコールバック関数を定義します。</span><span class="sxs-lookup"><span data-stu-id="20e66-105">Defines a callback function that MAPI calls to send an event notification.</span></span> <span data-ttu-id="20e66-106">このコールバック関数は [、HrAllocAdviseSink](hrallocadvisesink.md) 関数を呼び出して作成されたアアドバイス シンク オブジェクトにラップされた場合にのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="20e66-106">This callback function can only be used when wrapped in an advise sink object created by calling the [HrAllocAdviseSink](hrallocadvisesink.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="20e66-107">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="20e66-107">Header file:</span></span>  <br/> |<span data-ttu-id="20e66-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20e66-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="20e66-109">定義された関数は、次の方法で実装されます。</span><span class="sxs-lookup"><span data-stu-id="20e66-109">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="20e66-110">クライアント アプリケーションとサービス プロバイダー</span><span class="sxs-lookup"><span data-stu-id="20e66-110">Client applications and service providers</span></span>  <br/> |
|<span data-ttu-id="20e66-111">によって呼び出される定義済み関数:</span><span class="sxs-lookup"><span data-stu-id="20e66-111">Defined function called by:</span></span>  <br/> |<span data-ttu-id="20e66-112">MAPI</span><span class="sxs-lookup"><span data-stu-id="20e66-112">MAPI</span></span>  <br/> |
   
```cpp
ULONG (STDAPICALLTYPE NOTIFCALLBACK)(
  LPVOID lpvContext,
  ULONG cNotification,
  LPNOTIFICATION lpNotifications
);
```

## <a name="parameters"></a><span data-ttu-id="20e66-113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="20e66-113">Parameters</span></span>

 <span data-ttu-id="20e66-114">_lpvContext_</span><span class="sxs-lookup"><span data-stu-id="20e66-114">_lpvContext_</span></span>
  
> <span data-ttu-id="20e66-115">[in]MAPI がコールバック関数を呼び出す際にコールバック関数に渡される任意の値へのポインター。</span><span class="sxs-lookup"><span data-stu-id="20e66-115">[in] Pointer to an arbitrary value passed to the callback function when MAPI calls it.</span></span> <span data-ttu-id="20e66-116">この値は、クライアント アプリケーションまたはサービス プロバイダーにとって重要なアドレスを表します。</span><span class="sxs-lookup"><span data-stu-id="20e66-116">This value can represent an address of significance to the client application or service provider.</span></span> <span data-ttu-id="20e66-117">通常、C++ コードの場合  _、lpvContext_ パラメーターは C++ オブジェクトへのポインターを表します。</span><span class="sxs-lookup"><span data-stu-id="20e66-117">Typically, for C++ code, the  _lpvContext_ parameter represents a pointer to a C++ object.</span></span> 
    
 <span data-ttu-id="20e66-118">_cNotification_</span><span class="sxs-lookup"><span data-stu-id="20e66-118">_cNotification_</span></span>
  
> <span data-ttu-id="20e66-119">[in]  _lpNotifications_ パラメーターで示される配列内のイベント通知の数。</span><span class="sxs-lookup"><span data-stu-id="20e66-119">[in] Count of event notifications in the array indicated by the  _lpNotifications_ parameter.</span></span> 
    
 <span data-ttu-id="20e66-120">_lpNotifications_</span><span class="sxs-lookup"><span data-stu-id="20e66-120">_lpNotifications_</span></span>
  
> <span data-ttu-id="20e66-121">[out]この関数がイベント通知を含む [NOTIFICATION](notification.md) 構造体の配列を書き込む場所へのポインター。</span><span class="sxs-lookup"><span data-stu-id="20e66-121">[out] Pointer to the location where this function writes an array of [NOTIFICATION](notification.md) structures that contains the event notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20e66-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="20e66-122">Return value</span></span>

<span data-ttu-id="20e66-123">**NOTIFCALLBACK** 関数プロトタイプの有効な戻り値のセットは、関数がクライアント アプリケーションまたはサービス プロバイダーによって実装されるかどうかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="20e66-123">The set of valid return values for the **NOTIFCALLBACK** function prototype depends on whether the function is implemented by a client application or a service provider.</span></span> <span data-ttu-id="20e66-124">クライアントは常にクライアントを返S_OK。</span><span class="sxs-lookup"><span data-stu-id="20e66-124">Clients should always return S_OK.</span></span> <span data-ttu-id="20e66-125">プロバイダーは、ユーザーまたはS_OKをCALLBACK_DISCONTINUE。</span><span class="sxs-lookup"><span data-stu-id="20e66-125">Providers can return either S_OK or CALLBACK_DISCONTINUE.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="20e66-126">注釈</span><span class="sxs-lookup"><span data-stu-id="20e66-126">Remarks</span></span>

<span data-ttu-id="20e66-127">CALLBACK_DISCONTINUEは、同期コールバック関数の有効な戻り値です。MAPI は、この通知のコールバックの処理を直ちに停止する要求をします。</span><span class="sxs-lookup"><span data-stu-id="20e66-127">CALLBACK_DISCONTINUE is a valid return value for synchronous callback functions only; it requests that MAPI immediately stop processing the callbacks for this notification.</span></span> <span data-ttu-id="20e66-128">MAPI CALLBACK_DISCONTINUEが返される場合、MAPI は [IMAPISupport::Notify](imapisupport-notify.md)から返される _lpUlFlags_ パラメーターを NOTIFY_CANCELED に設定します。</span><span class="sxs-lookup"><span data-stu-id="20e66-128">When CALLBACK_DISCONTINUE is returned, MAPI sets the  _lpUlFlags_ parameter to NOTIFY_CANCELED when it returns from [IMAPISupport::Notify](imapisupport-notify.md).</span></span> 
  
<span data-ttu-id="20e66-129">同期コールバック関数で実行できる操作に関する制限を次に示します。</span><span class="sxs-lookup"><span data-stu-id="20e66-129">The following are limitations on what a synchronous callback function can do:</span></span>
  
- <span data-ttu-id="20e66-130">別の同期通知を生成することはできません。</span><span class="sxs-lookup"><span data-stu-id="20e66-130">It cannot cause another synchronous notification to be generated.</span></span>
    
- <span data-ttu-id="20e66-131">ユーザー インターフェイスを表示できません。</span><span class="sxs-lookup"><span data-stu-id="20e66-131">It cannot display a user interface.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20e66-132">関連項目</span><span class="sxs-lookup"><span data-stu-id="20e66-132">See also</span></span>



[<span data-ttu-id="20e66-133">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="20e66-133">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)

