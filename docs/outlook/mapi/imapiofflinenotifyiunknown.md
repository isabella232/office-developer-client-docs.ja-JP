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
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568148"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="2e913-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e913-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="2e913-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e913-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e913-105">通知コールバックをクライアントに送信するのには、Microsoft Outlook 2010 と Microsoft Outlook 2013 をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="2e913-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2e913-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="2e913-106">Provided by:</span></span>  <br/> |<span data-ttu-id="2e913-107">クライアント</span><span class="sxs-lookup"><span data-stu-id="2e913-107">Client</span></span>  <br/> |
|<span data-ttu-id="2e913-108">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="2e913-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2e913-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="2e913-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2e913-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="2e913-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2e913-111">Notify</span><span class="sxs-lookup"><span data-stu-id="2e913-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="2e913-112">接続状態の変更についてクライアントに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="2e913-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e913-113">注釈</span><span class="sxs-lookup"><span data-stu-id="2e913-113">Remarks</span></span>

<span data-ttu-id="2e913-114">クライアントは、このインターフェイスを実装し、 **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用してコールバックをセットアップするときの**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとして、それへのポインターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e913-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="2e913-115">その後、Outlook 2010 または Outlook 2013 できるようになります通知コールバックをクライアントに送信するのにはこのインターフェイスを使用します。</span><span class="sxs-lookup"><span data-stu-id="2e913-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2e913-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e913-116">See also</span></span>



[<span data-ttu-id="2e913-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="2e913-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="2e913-118">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="2e913-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="2e913-119">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="2e913-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2e913-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="2e913-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

