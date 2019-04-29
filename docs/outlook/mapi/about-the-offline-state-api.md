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
# <a name="about-the-offline-state-api"></a><span data-ttu-id="6f4c2-103">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="6f4c2-103">About the Offline State API</span></span>

  
  
<span data-ttu-id="6f4c2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6f4c2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6f4c2-105">オフライン状態 API は、microsoft outlook 2013 および microsoft outlook 2010 でユーザーの接続状態が変更されたことを示すコールバックをサポートします (たとえば、outlook 2013 または outlook 2010 でオフラインになっている場合)。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-105">The Offline State API supports callbacks indicating changes in a user's connection state in Microsoft Outlook 2013 and Microsoft Outlook 2010—for example, from being online in Outlook 2013 or Outlook 2010 to being offline.</span></span> <span data-ttu-id="6f4c2-106">この API は、outlook 2013 または outlook 2010 のグローバルオフラインオブジェクトを使用して、特定のユーザーアカウントプロファイルに対する変更を追跡します。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-106">The API uses a global offline object in Outlook 2013 or Outlook 2010 to track such changes for a given user account profile.</span></span> <span data-ttu-id="6f4c2-107">通知は、サポートされているコールバックの唯一の形式です。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-107">Notification is the only supported form of callback.</span></span> <span data-ttu-id="6f4c2-108">この API のクライアントとして、このような接続状態の変更を通知するメールプロバイダーは、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-108">As clients of this API, mail providers who want to be notified of such connection state changes do the following:</span></span>
  
1. <span data-ttu-id="6f4c2-109">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を実装します。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-109">Implement **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
2. <span data-ttu-id="6f4c2-110">**[hro・ offlineofflineobj](hropenofflineobj.md)** を使用して、特定のプロファイルの既存のオフラインオブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-110">Open an existing offline object for a specific profile using **[HrOpenOfflineObj](hropenofflineobj.md)**.</span></span> 
    
3. <span data-ttu-id="6f4c2-111">オブジェクトに、 **[imapioffline:: getcapabilities](imapioffline-getcapabilities.md)** を使用してオンラインまたはオフライン通知を提供する機能があるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-111">Determine if the object has the capability of providing online or offline notifications using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> 
    
4. <span data-ttu-id="6f4c2-112">**[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** を使用して、オブジェクトをオンライン通知またはオフライン通知用に登録します。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-112">Register the object for online or offline notifications using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="6f4c2-113">メールプロバイダーは、outlook 2013 または outlook 2010 で**IMAPIOfflineNotify**を使用して送信された通知を受信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-113">Mail providers can now receive notifications that Outlook 2013 or Outlook 2010 send using **IMAPIOfflineNotify**.</span></span> 
    
5. <span data-ttu-id="6f4c2-114">シャットダウン時に、 **[IMAPIOfflineMgr:: アドバイズ](imapiofflinemgr-unadvise.md)** 中止を使用してオンラインおよびオフライン通知の登録を削除します。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-114">On shutdown, remove registration for online and offline notifications using **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="6f4c2-115">一般に、outlook 2013 および outlook 2010 は、オンライン/オフライン変更のクライアントに加えて、他の変更を通知することができますが、オフライン状態 API はオンライン/オフラインの変更に関する通知のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-115">In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="6f4c2-116">クライアントは、他のすべての通知を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-116">The client should ignore all other notifications.</span></span> <span data-ttu-id="6f4c2-117">詳細については、「 **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-117">For more information, see **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**.</span></span> 
  
 <span data-ttu-id="6f4c2-118">オフライン状態 API を使用するクライアントの例については、「[サンプルのオフライン状態アドインについ](about-the-sample-offline-state-add-in.md)て」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-118">For an example of a client that uses the Offline State API, see [About the Sample Offline State Add-in](about-the-sample-offline-state-add-in.md).</span></span> <span data-ttu-id="6f4c2-119">サンプルのオフライン状態アドインは、オフライン状態 API を使用して接続状態を監視および変更する COM アドインです。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-119">The Sample Offline State Add-in is a COM add-in that uses the Offline State API to monitor and change the connection state.</span></span>
  
<span data-ttu-id="6f4c2-120">この API は、次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="6f4c2-120">This API provides the following:</span></span>
  
<span data-ttu-id="6f4c2-121">定義</span><span class="sxs-lookup"><span data-stu-id="6f4c2-121">Definitions:</span></span>
  
- [<span data-ttu-id="6f4c2-122">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="6f4c2-122">MAPI Constants</span></span>](mapi-constants.md)
    
<span data-ttu-id="6f4c2-123">データ型:</span><span class="sxs-lookup"><span data-stu-id="6f4c2-123">Data types:</span></span>
  
- <span data-ttu-id="6f4c2-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-124">**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**</span></span>
    
- <span data-ttu-id="6f4c2-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-125">**[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**</span></span>
    
- <span data-ttu-id="6f4c2-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-126">**[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**</span></span>
    
<span data-ttu-id="6f4c2-127">関数</span><span class="sxs-lookup"><span data-stu-id="6f4c2-127">Functions:</span></span>
  
- <span data-ttu-id="6f4c2-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-128">**[HrOpenOfflineObj](hropenofflineobj.md)**</span></span>
    
<span data-ttu-id="6f4c2-129">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="6f4c2-129">Interfaces:</span></span>
  
- <span data-ttu-id="6f4c2-130">**[imapioffline](imapiofflineiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-130">**[IMAPIOffline](imapiofflineiunknown.md)**</span></span>
    
- <span data-ttu-id="6f4c2-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-131">**[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**</span></span>
    
- <span data-ttu-id="6f4c2-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="6f4c2-132">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**</span></span>
    

