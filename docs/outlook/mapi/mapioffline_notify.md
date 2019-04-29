---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 6c5480a8f5e008c01c7ab8141317f5f19547ab10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414768"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="5964a-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="5964a-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="5964a-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5964a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5964a-105">これは、接続状態の変更に対する通知です。</span><span class="sxs-lookup"><span data-stu-id="5964a-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="5964a-106">この値は、変更された接続状態の部分、古い接続状態、および新しい接続状態を示します。</span><span class="sxs-lookup"><span data-stu-id="5964a-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="5964a-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="5964a-107">Quick info</span></span>

<span data-ttu-id="5964a-108">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5964a-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef struct  
{ 
      ULONG ulSize; 
      MAPIOFFLINE_NOTIFY_TYPE NotifyType; 
      ULONG ulClientToken; 
      union { 
         struct 
           { 
           ULONG ulMask; 
           ULONG ulStateOld; 
           ULONG ulStateNew; 
           } StateChange; 
             } Info; 
} MAPIOFFLINE_NOTIFY;
```

## <a name="members"></a><span data-ttu-id="5964a-109">メンバー</span><span class="sxs-lookup"><span data-stu-id="5964a-109">Members</span></span>

 <span data-ttu-id="5964a-110">_ulsize_</span><span class="sxs-lookup"><span data-stu-id="5964a-110">_ulSize_</span></span>
  
> <span data-ttu-id="5964a-111">**MAPIOFFLINE_NOTIFY**構造体のサイズ。</span><span class="sxs-lookup"><span data-stu-id="5964a-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="5964a-112">_notifytype_</span><span class="sxs-lookup"><span data-stu-id="5964a-112">_NotifyType_</span></span>
  
> <span data-ttu-id="5964a-113">通知の種類。</span><span class="sxs-lookup"><span data-stu-id="5964a-113">Type of notification.</span></span> <span data-ttu-id="5964a-114">接続状態の変更に関する通知のみがサポートされることに注意してください。サポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5964a-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="5964a-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="5964a-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="5964a-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="5964a-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="5964a-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="5964a-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="5964a-118">_ulclienttoken_</span><span class="sxs-lookup"><span data-stu-id="5964a-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="5964a-119">**[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)** の**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** 構造でクライアントによって定義されたトークン。</span><span class="sxs-lookup"><span data-stu-id="5964a-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="5964a-120">_ulmask_</span><span class="sxs-lookup"><span data-stu-id="5964a-120">_ulMask_</span></span>
  
> <span data-ttu-id="5964a-121">変更された接続状態の部分。</span><span class="sxs-lookup"><span data-stu-id="5964a-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="5964a-122">サポートされている値は MAPIOFFLINE_STATE_OFFLINE_MASK のみです。</span><span class="sxs-lookup"><span data-stu-id="5964a-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="5964a-123">_ulstateold_</span><span class="sxs-lookup"><span data-stu-id="5964a-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="5964a-124">古い接続状態。</span><span class="sxs-lookup"><span data-stu-id="5964a-124">The old connection state.</span></span> <span data-ttu-id="5964a-125">サポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5964a-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="5964a-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5964a-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="5964a-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5964a-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="5964a-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="5964a-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="5964a-129">新しい接続状態。</span><span class="sxs-lookup"><span data-stu-id="5964a-129">The new connection state.</span></span> <span data-ttu-id="5964a-130">サポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="5964a-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="5964a-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="5964a-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="5964a-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="5964a-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5964a-133">注釈</span><span class="sxs-lookup"><span data-stu-id="5964a-133">Remarks</span></span>

<span data-ttu-id="5964a-134">オフライン状態 API は、オンライン/オフラインの変更についてのみ通知をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="5964a-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="5964a-135">クライアントは、実際の変更を検査する前に、Outlook が次の値を返すことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5964a-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="5964a-136">*notifytype*には、値 MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE、または MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE があります。</span><span class="sxs-lookup"><span data-stu-id="5964a-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="5964a-137">この例では、クライアントは、変更が接続状態の変更であると想定し、 *Info*は*StateChange*構造になっています。</span><span class="sxs-lookup"><span data-stu-id="5964a-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="5964a-138">*ulmask*の値は MAPIOFFLINE_STATE_OFFLINE_MASK です。</span><span class="sxs-lookup"><span data-stu-id="5964a-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="5964a-139">この場合、クライアントは、変更がオンライン/オフラインの接続状態に変更されたと見なすことができ、 *ulstateold*および*ulStateNew*の調査に進むことができます。</span><span class="sxs-lookup"><span data-stu-id="5964a-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="5964a-140">Outlook は、サポートされていない他の変更をクライアントに通知することができます。</span><span class="sxs-lookup"><span data-stu-id="5964a-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="5964a-141">このような場合、 *notifytype*は、前に示した3つの値のいずれかにはなりません。また*ulmask*は MAPIOFFLINE_STATE_OFFLINE_MASK されず、クライアントは*Info*の残りのデータを無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5964a-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5964a-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="5964a-142">See also</span></span>

- [<span data-ttu-id="5964a-143">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="5964a-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="5964a-144">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="5964a-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="5964a-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="5964a-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

