---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 37f21c438a0a337eecf5c15a27a0b891d19bcfb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19800632"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="7f9cb-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7f9cb-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="7f9cb-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7f9cb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7f9cb-105">通知コールバックをクライアントに送信するのには、Microsoft Outlook 2010 と Microsoft Outlook 2013 をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="7f9cb-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f9cb-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="7f9cb-106">Provided by:</span></span>  <br/> |<span data-ttu-id="7f9cb-107">クライアント</span><span class="sxs-lookup"><span data-stu-id="7f9cb-107">Client</span></span>  <br/> |
|<span data-ttu-id="7f9cb-108">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7f9cb-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7f9cb-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="7f9cb-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7f9cb-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7f9cb-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7f9cb-111">Notify</span><span class="sxs-lookup"><span data-stu-id="7f9cb-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="7f9cb-112">接続状態の変更についてクライアントに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="7f9cb-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f9cb-113">注釈</span><span class="sxs-lookup"><span data-stu-id="7f9cb-113">Remarks</span></span>

<span data-ttu-id="7f9cb-114">クライアントは、このインターフェイスを実装し、 **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用してコールバックをセットアップするときの**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとして、それへのポインターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="7f9cb-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="7f9cb-115">その後、Outlook 2010 または Outlook 2013 できるようになります通知コールバックをクライアントに送信するのにはこのインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="7f9cb-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7f9cb-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="7f9cb-116">See also</span></span>



[<span data-ttu-id="7f9cb-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="7f9cb-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="7f9cb-118">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="7f9cb-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="7f9cb-119">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="7f9cb-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="7f9cb-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="7f9cb-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

