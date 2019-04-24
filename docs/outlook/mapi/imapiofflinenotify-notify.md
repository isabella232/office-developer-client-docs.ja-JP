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
ms.openlocfilehash: 4440df4b8e4a46e13748cf47d599e16599aaf858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270085"
---
# <a name="imapiofflinenotifynotify"></a><span data-ttu-id="43528-103">IMAPIOfflineNotify::Notify</span><span class="sxs-lookup"><span data-stu-id="43528-103">IMAPIOfflineNotify::Notify</span></span>

  
  
<span data-ttu-id="43528-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="43528-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="43528-105">接続状態の変更についてクライアントに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="43528-105">Sends notifications to the client about changes in connection state.</span></span>
  
```cpp
void STDMETHODCALLTYPE Notify(  
    const MAPIOFFLINE_NOTIFY * pNotifyInfo 
);
```

## <a name="parameters"></a><span data-ttu-id="43528-106">パラメーター</span><span class="sxs-lookup"><span data-stu-id="43528-106">Parameters</span></span>

 <span data-ttu-id="43528-107">_pnotifyinfo_</span><span class="sxs-lookup"><span data-stu-id="43528-107">_pNotifyInfo_</span></span>
  
> <span data-ttu-id="43528-108">順番Outlook からクライアントに送信される通知。</span><span class="sxs-lookup"><span data-stu-id="43528-108">[in] The notification that Outlook sends to the client.</span></span> <span data-ttu-id="43528-109">通知は、変更された接続状態の一部、古い接続状態、および新しい接続状態を示します。</span><span class="sxs-lookup"><span data-stu-id="43528-109">The notification indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="43528-110">解説</span><span class="sxs-lookup"><span data-stu-id="43528-110">Remarks</span></span>

<span data-ttu-id="43528-111">Outlook では、このメソッドを使用して通知コールバックをクライアントに送信します。</span><span class="sxs-lookup"><span data-stu-id="43528-111">Outlook uses this method to send notification callbacks to a client.</span></span> <span data-ttu-id="43528-112">このインターフェイスを microsoft outlook 2010 または microsoft outlook 2013 が使用できるようにするには、クライアントはこのインターフェイスを実装し、 **[](mapioffline_adviseinfo.md)** **[IMAPIOfflineMgr:: Advise を使用してコールバックを設定するときに、MAPIOFFLINE_ADVISEINFO のメンバーとしてのポインターを渡す必要があります。](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="43528-112">To make this interface available to Microsoft Outlook 2010 or Microsoft Outlook 2013, the client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
  
<span data-ttu-id="43528-113">また、クライアントは、outlook 2010 または outlook 2013 が**IMAPIOfflineNotify:: Notify**で使用するクライアントトークンを**MAPIOFFLINE_ADVISEINFO**に渡して、通知コールバック用に登録されているクライアントを識別します。</span><span class="sxs-lookup"><span data-stu-id="43528-113">The client also passes to **MAPIOFFLINE_ADVISEINFO** a client token that Outlook 2010 or Outlook 2013 uses in **IMAPIOfflineNotify::Notify** to identify the client registered for the notification callback.</span></span> 
  
<span data-ttu-id="43528-114">一般に、outlook 2010 および outlook 2013 は、オンライン/オフラインの変更やその他の接続状態の変更をクライアントに通知します。ただし、オフライン状態 API はオンライン/オフラインの変更に関する通知のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="43528-114">In general, Outlook 2010 and Outlook 2013 can notify a client of online/offline changes and other connection state changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="43528-115">クライアントは、他のすべての通知を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="43528-115">The client must ignore all other notifications.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="43528-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="43528-116">See also</span></span>



[<span data-ttu-id="43528-117">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="43528-117">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="43528-118">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="43528-118">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

