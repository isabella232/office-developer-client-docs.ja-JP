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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270309"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="cd574-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cd574-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="cd574-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cd574-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cd574-105">microsoft outlook 2010 および microsoft outlook 2013 をサポートしており、クライアントに対して通知コールバックを送信します。</span><span class="sxs-lookup"><span data-stu-id="cd574-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cd574-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="cd574-106">Provided by:</span></span>  <br/> |<span data-ttu-id="cd574-107">クライアント</span><span class="sxs-lookup"><span data-stu-id="cd574-107">Client</span></span>  <br/> |
|<span data-ttu-id="cd574-108">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="cd574-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cd574-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="cd574-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cd574-110">v の順序</span><span class="sxs-lookup"><span data-stu-id="cd574-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cd574-111">Notify</span><span class="sxs-lookup"><span data-stu-id="cd574-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="cd574-112">接続状態の変更についてクライアントに通知を送信します。</span><span class="sxs-lookup"><span data-stu-id="cd574-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd574-113">解説</span><span class="sxs-lookup"><span data-stu-id="cd574-113">Remarks</span></span>

<span data-ttu-id="cd574-114">**[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** を使用してコールバックを設定する場合、クライアントはこのインターフェイスを実装し、 **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** のメンバーとしてのポインターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="cd574-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="cd574-115">その後、outlook 2010 または outlook 2013 は、このインターフェイスを使用して、クライアントに通知コールバックを送信できるようになります。</span><span class="sxs-lookup"><span data-stu-id="cd574-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cd574-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="cd574-116">See also</span></span>



[<span data-ttu-id="cd574-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="cd574-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="cd574-118">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="cd574-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="cd574-119">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="cd574-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="cd574-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="cd574-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

