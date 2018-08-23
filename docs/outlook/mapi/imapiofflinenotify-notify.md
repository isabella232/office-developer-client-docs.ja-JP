---
title: IMAPIOfflineNotifyNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify.Notify
api_type:
- COM
ms.assetid: 10c7cb9d-2e9d-72eb-6b07-31eed892e646
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 54843339c6843e075ec769da5751ae2fe753f302
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800644"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="1c373-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="1c373-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="1c373-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1c373-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1c373-105">接続状態の変更についてクライアントに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="1c373-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="1c373-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1c373-106">Parameters</span></span>

 <span data-ttu-id="1c373-107">_pNotifyInfo_</span><span class="sxs-lookup"><span data-stu-id="1c373-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="1c373-108">[in]Outlook をクライアントに送信する通知します。</span><span class="sxs-lookup"><span data-stu-id="1c373-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="1c373-109">通知では、接続状態が変更されたこと、以前の接続状態、および新しい接続の状態の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="1c373-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1c373-110">注釈</span><span class="sxs-lookup"><span data-stu-id="1c373-110">Remarks</span></span>

<span data-ttu-id="1c373-111">Outlook では、このメソッドを使用して、通知のコールバックをクライアントに送信します。</span><span class="sxs-lookup"><span data-stu-id="1c373-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="1c373-112">Microsoft Outlook 2010 または Microsoft Outlook 2013 にこのインターフェイスを使用できるようにするには、クライアントする必要がありますこのインターフェイスを実装し、 **[IMAPIOfflineMgr::Advise を使用してコールバックをセットアップするときの**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとして、それへのポインターを渡す](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="1c373-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="1c373-113">クライアントもトークンを渡します**MAPIOFFLINE_ADVISEINFO**に、クライアントを Outlook 2010 または Outlook 2013 では、 **IMAPIOfflineNotify::Notify**の通知コールバックの登録されているクライアントを識別します。</span><span class="sxs-lookup"><span data-stu-id="1c373-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="1c373-114">一般に、Outlook 2010、Outlook 2013 は、オンラインとオフラインの変更のクライアントおよびその他の接続状態の変更を通知できますが、オフライン状態の API は、オンラインとオフラインの変更の通知のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="1c373-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="1c373-115">クライアントは、他のすべての通知を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1c373-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1c373-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="1c373-116">See also</span></span>



[<span data-ttu-id="1c373-117">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="1c373-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="1c373-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="1c373-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

