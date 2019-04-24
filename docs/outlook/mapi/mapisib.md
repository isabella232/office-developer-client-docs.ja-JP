---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270211"
---
# <a name="mapisib"></a><span data-ttu-id="f93a4-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="f93a4-103">MAPISIB</span></span>

  
  
<span data-ttu-id="f93a4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f93a4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f93a4-105">この構造体は、 [imapisync:: SynchronizeInBackground](imapisyncsynchronizeinbackground.md)で使用されます。</span><span class="sxs-lookup"><span data-stu-id="f93a4-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
```cpp
typedef struct _MAPISIB
{
ULONG           ulSize;                
ULONG           ulFlags;
LPMAPISESSION   psesSync;
LPUNKNOWN       punkCallBack;
HANDLE          *phSyncDoneEvent;    
} MAPISIB, *PMAPISIB
```

## <a name="members"></a><span data-ttu-id="f93a4-106">Members</span><span class="sxs-lookup"><span data-stu-id="f93a4-106">Members</span></span>

 <span data-ttu-id="f93a4-107">**ulsize**</span><span class="sxs-lookup"><span data-stu-id="f93a4-107">**ulSize**</span></span>
  
> <span data-ttu-id="f93a4-108">構造体のサイズ。</span><span class="sxs-lookup"><span data-stu-id="f93a4-108">The size of the structure.</span></span>
    
 <span data-ttu-id="f93a4-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="f93a4-109">**ulFlags**</span></span>
  
> <span data-ttu-id="f93a4-110">同期の種類を示すフラグ。次のいずれかの値であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="f93a4-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="f93a4-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="f93a4-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="f93a4-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="f93a4-112">0x00000200</span></span>  <br/> |<span data-ttu-id="f93a4-113">メッセージをサーバーに送信します (現在は使用されていません)。</span><span class="sxs-lookup"><span data-stu-id="f93a4-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="f93a4-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="f93a4-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="f93a4-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="f93a4-115">0x00000001</span></span>  <br/> |<span data-ttu-id="f93a4-116">サーバーに対して階層の変更を行います。</span><span class="sxs-lookup"><span data-stu-id="f93a4-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="f93a4-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="f93a4-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="f93a4-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="f93a4-118">0x00000002</span></span>  <br/> |<span data-ttu-id="f93a4-119">サーバーから階層の変更を取得します。</span><span class="sxs-lookup"><span data-stu-id="f93a4-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="f93a4-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="f93a4-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="f93a4-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="f93a4-121">0x00000040</span></span>  <br/> |<span data-ttu-id="f93a4-122">メッセージの変更をサーバーにプッシュします。</span><span class="sxs-lookup"><span data-stu-id="f93a4-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="f93a4-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="f93a4-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="f93a4-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="f93a4-124">0x00000080</span></span>  <br/> |<span data-ttu-id="f93a4-125">サーバーからメッセージの変更を取得します。</span><span class="sxs-lookup"><span data-stu-id="f93a4-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="f93a4-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="f93a4-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="f93a4-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="f93a4-127">0x20000000</span></span>  <br/> |<span data-ttu-id="f93a4-128">同期はユーザーによって開始され、より高い優先度である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f93a4-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="f93a4-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="f93a4-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="f93a4-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="f93a4-130">0x02000000</span></span>  <br/> |<span data-ttu-id="f93a4-131">完全な本文ではなく、ヘッダーのみを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f93a4-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="f93a4-132">**p' sync**</span><span class="sxs-lookup"><span data-stu-id="f93a4-132">**psesSync**</span></span>
  
> <span data-ttu-id="f93a4-133">順番MAPI セッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f93a4-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="f93a4-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="f93a4-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="f93a4-135">順番進行状況を提供するインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="f93a4-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="f93a4-136">[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)のインターフェイスを照会するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="f93a4-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="f93a4-137">**\*phsyncdoneevent**</span><span class="sxs-lookup"><span data-stu-id="f93a4-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="f93a4-138">読み上げ作成されたスレッドが完了したときに発生するイベント。</span><span class="sxs-lookup"><span data-stu-id="f93a4-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="f93a4-139">このポインターは、イベントが含まれるため、有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="f93a4-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f93a4-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="f93a4-140">See also</span></span>



[<span data-ttu-id="f93a4-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f93a4-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="f93a4-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f93a4-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

