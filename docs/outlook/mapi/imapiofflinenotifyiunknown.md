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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439878"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="38fdc-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="38fdc-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="38fdc-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38fdc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38fdc-105">クライアントMicrosoft Outlook 2010コールバックMicrosoft Outlook 2013送信する方法をサポートします。</span><span class="sxs-lookup"><span data-stu-id="38fdc-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="38fdc-106">提供元:</span><span class="sxs-lookup"><span data-stu-id="38fdc-106">Provided by:</span></span>  <br/> |<span data-ttu-id="38fdc-107">クライアント</span><span class="sxs-lookup"><span data-stu-id="38fdc-107">Client</span></span>  <br/> |
|<span data-ttu-id="38fdc-108">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="38fdc-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="38fdc-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="38fdc-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="38fdc-110">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="38fdc-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="38fdc-111">Notify</span><span class="sxs-lookup"><span data-stu-id="38fdc-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="38fdc-112">接続状態の変更に関する通知をクライアントに送信します。</span><span class="sxs-lookup"><span data-stu-id="38fdc-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38fdc-113">注釈</span><span class="sxs-lookup"><span data-stu-id="38fdc-113">Remarks</span></span>

<span data-ttu-id="38fdc-114">**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** を使用してコールバックを設定する **[](mapioffline_adviseinfo.md)** 場合、クライアントは、このインターフェイスを実装し、MAPIOFFLINE_ADVISEINFO でメンバーとしてポインターを渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="38fdc-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="38fdc-115">その後Outlook 2010 または Outlook 2013 では、このインターフェイスを使用してクライアントに通知コールバックを送信できます。</span><span class="sxs-lookup"><span data-stu-id="38fdc-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="38fdc-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="38fdc-116">See also</span></span>



[<span data-ttu-id="38fdc-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="38fdc-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="38fdc-118">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="38fdc-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="38fdc-119">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="38fdc-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="38fdc-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="38fdc-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

