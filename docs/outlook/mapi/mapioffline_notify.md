---
title: MAPIOFFLINE_NOTIFY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e03c5a87-4513-2133-ae0a-11d242f80e4b
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: b18a4ae4ee25898d1100d9763714e5be21c69fd8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580727"
---
# <a name="mapiofflinenotify"></a><span data-ttu-id="08290-103">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="08290-103">MAPIOFFLINE_NOTIFY</span></span>

<span data-ttu-id="08290-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08290-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08290-105">これは、接続状態の変更を通知します。</span><span class="sxs-lookup"><span data-stu-id="08290-105">This is the notification for a change in the connection state.</span></span> <span data-ttu-id="08290-106">接続状態が変更されたこと、以前の接続状態、および新しい接続の状態の一部を示します。</span><span class="sxs-lookup"><span data-stu-id="08290-106">It indicates the part of the connection state that has changed, the old connection state, and the new connection state.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="08290-107">クイック ヒント</span><span class="sxs-lookup"><span data-stu-id="08290-107">Quick info</span></span>

<span data-ttu-id="08290-108">**[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** を参照してください。</span><span class="sxs-lookup"><span data-stu-id="08290-108">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="08290-109">Members</span><span class="sxs-lookup"><span data-stu-id="08290-109">Members</span></span>

 <span data-ttu-id="08290-110">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="08290-110">_ulSize_</span></span>
  
> <span data-ttu-id="08290-111">**MAPIOFFLINE_NOTIFY**構造体のサイズです。</span><span class="sxs-lookup"><span data-stu-id="08290-111">Size of the **MAPIOFFLINE_NOTIFY** structure.</span></span> 
    
 <span data-ttu-id="08290-112">_NotifyType_</span><span class="sxs-lookup"><span data-stu-id="08290-112">_NotifyType_</span></span>
  
> <span data-ttu-id="08290-113">通知の種類です。</span><span class="sxs-lookup"><span data-stu-id="08290-113">Type of notification.</span></span> <span data-ttu-id="08290-114">接続状態の変更時にのみ通知がサポートされることに注意してください。のみサポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="08290-114">Note that only notification on change of the connection state is supported; the only supported values are:</span></span>
    
   - <span data-ttu-id="08290-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span><span class="sxs-lookup"><span data-stu-id="08290-115">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START</span></span>
    
   - <span data-ttu-id="08290-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span><span class="sxs-lookup"><span data-stu-id="08290-116">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE</span></span>
    
   - <span data-ttu-id="08290-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span><span class="sxs-lookup"><span data-stu-id="08290-117">MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE</span></span>
    
 <span data-ttu-id="08290-118">_ulClientToken_</span><span class="sxs-lookup"><span data-stu-id="08290-118">_ulClientToken_</span></span>
  
> <span data-ttu-id="08290-119">クライアントが**[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** の**[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** 構造体で定義されているトークンです。</span><span class="sxs-lookup"><span data-stu-id="08290-119">A token defined by the client in the **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** structure in **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> 
    
 <span data-ttu-id="08290-120">_ulMask_</span><span class="sxs-lookup"><span data-stu-id="08290-120">_ulMask_</span></span>
  
> <span data-ttu-id="08290-121">接続の状態が変更されたことの一部です。</span><span class="sxs-lookup"><span data-stu-id="08290-121">The part of the connection state that has changed.</span></span> <span data-ttu-id="08290-122">唯一のサポートされている値は、MAPIOFFLINE_STATE_OFFLINE_MASK です。</span><span class="sxs-lookup"><span data-stu-id="08290-122">The only supported value is MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span>
    
 <span data-ttu-id="08290-123">_ulStateOld_</span><span class="sxs-lookup"><span data-stu-id="08290-123">_ulStateOld_</span></span>
  
> <span data-ttu-id="08290-124">古い接続状態です。</span><span class="sxs-lookup"><span data-stu-id="08290-124">The old connection state.</span></span> <span data-ttu-id="08290-125">のみサポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="08290-125">The only supported values are:</span></span>
    
   - <span data-ttu-id="08290-126">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="08290-126">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="08290-127">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="08290-127">MAPIOFFLINE_STATE_ONLINE</span></span>
    
 <span data-ttu-id="08290-128">_ulStateNew_</span><span class="sxs-lookup"><span data-stu-id="08290-128">_ulStateNew_</span></span>
  
> <span data-ttu-id="08290-129">新しい接続状態です。</span><span class="sxs-lookup"><span data-stu-id="08290-129">The new connection state.</span></span> <span data-ttu-id="08290-130">のみサポートされている値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="08290-130">The only supported values are:</span></span>
    
   - <span data-ttu-id="08290-131">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="08290-131">MAPIOFFLINE_STATE_OFFLINE</span></span>
    
   - <span data-ttu-id="08290-132">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="08290-132">MAPIOFFLINE_STATE_ONLINE</span></span>
    
## <a name="remarks"></a><span data-ttu-id="08290-133">注釈</span><span class="sxs-lookup"><span data-stu-id="08290-133">Remarks</span></span>

<span data-ttu-id="08290-134">オフラインの状態の API では、オンラインとオフラインの変更の通知のみをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="08290-134">The Offline State API supports only notifications for online/offline changes.</span></span> <span data-ttu-id="08290-135">クライアントは、Outlook が実際の変更を確認する前に次の値を返すことを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08290-135">A client must check that Outlook returns the following values before examining the actual change:</span></span>
  
1.  <span data-ttu-id="08290-136">*NotifyType*には、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START、MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE、または MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE の値があります。</span><span class="sxs-lookup"><span data-stu-id="08290-136">*NotifyType*  has the value MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START, MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE, or MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE.</span></span> <span data-ttu-id="08290-137">この例では、クライアントは、変更は、接続状態の変更*の*構造体の*情報*と想定できます。</span><span class="sxs-lookup"><span data-stu-id="08290-137">In this case, the client can assume that the change is a connection state change, and  *Info*  is of the structure  *StateChange*  .</span></span> 
    
2.  <span data-ttu-id="08290-138">*ulMask*には、MAPIOFFLINE_STATE_OFFLINE_MASK の値があります。</span><span class="sxs-lookup"><span data-stu-id="08290-138">*ulMask*  has the value MAPIOFFLINE_STATE_OFFLINE_MASK.</span></span> <span data-ttu-id="08290-139">この例では、クライアントは、オンラインとオフラインの接続状態の変更、および*ulStateOld*と*ulStateNew*の確認を行うことを想定できます。</span><span class="sxs-lookup"><span data-stu-id="08290-139">In this case, the client can assume that the change is an online/offline connection state change, and can proceed with examining  *ulStateOld*  and  *ulStateNew*  .</span></span> 
    
<span data-ttu-id="08290-140">Outlook がサポートされていないその他の変更のクライアントに通知することができます。</span><span class="sxs-lookup"><span data-stu-id="08290-140">It is possible that Outlook notifies a client of other changes that are not supported.</span></span> <span data-ttu-id="08290-141">このような場合、 *NotifyType*できません、上記 3 つの値のいずれかのや*ulMask*には、MAPIOFFLINE_STATE_OFFLINE_MASK ができないクライアントは、*情報*では、データの残りの部分を無視する必要があります。</span><span class="sxs-lookup"><span data-stu-id="08290-141">In such cases,  *NotifyType*  would not be any one of the three values stated previously, or  *ulMask*  would not be MAPIOFFLINE_STATE_OFFLINE_MASK, and the client must ignore the rest of the data in  *Info*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="08290-142">関連項目</span><span class="sxs-lookup"><span data-stu-id="08290-142">See also</span></span>

- [<span data-ttu-id="08290-143">オフライン状態 API について</span><span class="sxs-lookup"><span data-stu-id="08290-143">About the Offline State API</span></span>](about-the-offline-state-api.md)  
- [<span data-ttu-id="08290-144">MAPI �萔</span><span class="sxs-lookup"><span data-stu-id="08290-144">MAPI Constants</span></span>](mapi-constants.md)  
- [<span data-ttu-id="08290-145">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="08290-145">MAPIOFFLINE_NOTIFY_TYPE</span></span>](mapioffline_notify_type.md)

