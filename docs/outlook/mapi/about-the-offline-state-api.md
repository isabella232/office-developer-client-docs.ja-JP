---
title: オフラインの状態の API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19799623"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="f1ab5-103">オフラインの状態の API について</span><span class="sxs-lookup"><span data-stu-id="f1ab5-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="f1ab5-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f1ab5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f1ab5-105">オフラインの状態の API は、Microsoft Outlook 2013 および Microsoft Outlook 2010 でのユーザーの接続状態の変化を示すコールバックをサポートしています: からのオフライン中に Outlook 2013 または Outlook 2010 でオンラインにします。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="f1ab5-106">API は、特定のユーザー ・ アカウント ・ プロファイルには、このような変更を追跡するために Outlook 2013 または Outlook 2010 でのオフラインのグローバル オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="f1ab5-107">通知は、コールバックの形式でのみサポートされています。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="f1ab5-108">この API のクライアントとしてこのような接続状態の変更の通知を受ける必要があるメールのプロバイダー、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="f1ab5-109">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を実装します。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="f1ab5-110">**[HrOpenOfflineObj](hropenofflineobj.md)** を使用して特定のプロファイルに既存のオフライン オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="f1ab5-111">オブジェクトに**[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用して、オンラインまたはオフラインの通知を提供する機能があるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="f1ab5-112">**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用して通知をオンラインまたはオフラインのオブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="f1ab5-113">メール プロバイダーでは、2013 の Outlook または Outlook 2010 送信する**IMAPIOfflineNotify**を使用して通知を受信できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="f1ab5-114">シャット ダウン時に**[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** を使用して、オンラインとオフラインの通知の登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="f1ab5-115">一般に、Outlook 2013 と Outlook 2010 のオンライン/オフラインでの変更とその他の変更は、クライアントに通知できますが、オフライン状態の API は、オンラインとオフラインの変更の通知のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="f1ab5-116">クライアントは、他のすべての通知を無視してください。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="f1ab5-117">詳細については、 **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** および**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="f1ab5-118">オフライン状態 API を使用するクライアントの例は、[のサンプル オフライン状態がアドインを](about-the-sample-offline-state-add-in.md)参照してください。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="f1ab5-119">オフライン状態のサンプル アドインは、COM アドインの API を使用して、オフラインの状態を監視し、接続状態を変更します。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="f1ab5-120">この API には、次のものが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f1ab5-120">This API provides the following:</span></span>
  
<span data-ttu-id="f1ab5-121">定義</span><span class="sxs-lookup"><span data-stu-id="f1ab5-121">Definitions:</span></span>
  
- [<span data-ttu-id="f1ab5-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="f1ab5-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="f1ab5-123">データ型:</span><span class="sxs-lookup"><span data-stu-id="f1ab5-123">Data types:</span></span>
  
- <span data-ttu-id="f1ab5-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="f1ab5-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="f1ab5-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="f1ab5-127">関数</span><span class="sxs-lookup"><span data-stu-id="f1ab5-127">Functions:</span></span>
  
- <span data-ttu-id="f1ab5-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="f1ab5-129">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="f1ab5-129">Interfaces:</span></span>
  
- <span data-ttu-id="f1ab5-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="f1ab5-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="f1ab5-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="f1ab5-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

