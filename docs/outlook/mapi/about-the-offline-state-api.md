---
title: オフライン状態 API について
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ŏI�X�V��: 2012�N6��25��'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410484"
---
# <a name="about-the-offline-state-api"></a><span data-ttu-id="c5683-103">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="c5683-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="c5683-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c5683-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c5683-105">オフライン状態 API は、Microsoft Outlook 2013 および Microsoft Outlook 2010 でのユーザーの接続状態の変更を示すコールバックをサポートしています 。たとえば、Outlook 2013 または Outlook 2010 のオンライン状態からオフライン状態に変わるなどです。</span><span class="sxs-lookup"><span data-stu-id="c5683-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="c5683-106">API は、2013 年または Outlook 2010 年Outlookにグローバル オフライン オブジェクトを使用して、特定のユーザー アカウント プロファイルに対するこのような変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="c5683-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="c5683-107">通知は、サポートされているコールバックの唯一の形式です。</span><span class="sxs-lookup"><span data-stu-id="c5683-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="c5683-108">この API のクライアントとして、このような接続状態の変更を通知するメール プロバイダーは次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="c5683-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="c5683-109">**[IMAPIOfflineNotify を実装します](imapiofflinenotifyiunknown.md)**。</span><span class="sxs-lookup"><span data-stu-id="c5683-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="c5683-110">**[HrOpenOfflineObj](hropenofflineobj.md)** を使用して、特定のプロファイルの既存のオフライン オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="c5683-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="c5683-111">オブジェクトが **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)** を使用してオンライン通知またはオフライン通知を提供できるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="c5683-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="c5683-112">**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用して、オンラインまたはオフラインの通知のオブジェクトを登録します。</span><span class="sxs-lookup"><span data-stu-id="c5683-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="c5683-113">メール プロバイダーは **、IMAPIOfflineNotify** を使用して 2013 Outlook 2010 Outlook通知を受信できます。</span><span class="sxs-lookup"><span data-stu-id="c5683-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="c5683-114">シャットダウン時に **[、IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)** を使用してオンライン通知とオフライン通知の登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="c5683-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="c5683-115">一般に、Outlook 2013 および Outlook 2010 は、オンライン/オフラインの変更と他の変更をクライアントに通知できますが、オフライン状態 API では、オンライン/オフラインの変更に関する通知のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="c5683-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="c5683-116">クライアントは、他のすべての通知を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c5683-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="c5683-117">詳細については **[、「IMAPIOfflineNotify::Notify and MAPIOFFLINE_NOTIFY」](imapiofflinenotify-notify.md)** **[を参照してください](mapioffline_notify.md)**。</span><span class="sxs-lookup"><span data-stu-id="c5683-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="c5683-118">オフライン状態 API を使用するクライアントの例については、「サンプル オフライン状態アドインについて」 [を参照してください](about-the-sample-offline-state-add-in.md)。</span><span class="sxs-lookup"><span data-stu-id="c5683-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="c5683-119">サンプル オフライン状態アドインは、オフライン状態 API を使用して接続状態を監視および変更する COM アドインです。</span><span class="sxs-lookup"><span data-stu-id="c5683-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="c5683-120">この API は、次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="c5683-120">This API provides the following:</span></span>
  
<span data-ttu-id="c5683-121">定義:</span><span class="sxs-lookup"><span data-stu-id="c5683-121">Definitions:</span></span>
  
- [<span data-ttu-id="c5683-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="c5683-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="c5683-123">データ型:</span><span class="sxs-lookup"><span data-stu-id="c5683-123">Data types:</span></span>
  
- <span data-ttu-id="c5683-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="c5683-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="c5683-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="c5683-127">関数</span><span class="sxs-lookup"><span data-stu-id="c5683-127">Functions:</span></span>
  
- <span data-ttu-id="c5683-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="c5683-129">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="c5683-129">Interfaces:</span></span>
  
- <span data-ttu-id="c5683-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="c5683-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="c5683-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="c5683-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

