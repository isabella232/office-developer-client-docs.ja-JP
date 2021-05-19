---
title: MAPISIB
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 16452798-7a95-43da-b95e-908debcea050
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: cbda978a0d69367e95f9b4b1f53fd6d03b113ccc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418709"
---
# <a name="mapisib"></a><span data-ttu-id="26dd4-103">MAPISIB</span><span class="sxs-lookup"><span data-stu-id="26dd4-103">MAPISIB</span></span>

  
  
<span data-ttu-id="26dd4-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26dd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26dd4-105">この構造は [IMAPISync::SyncInBackground と一緒に使用されます](imapisyncsynchronizeinbackground.md)。</span><span class="sxs-lookup"><span data-stu-id="26dd4-105">This structure is used with [IMAPISync::SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span>
  
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

## <a name="members"></a><span data-ttu-id="26dd4-106">Members</span><span class="sxs-lookup"><span data-stu-id="26dd4-106">Members</span></span>

 <span data-ttu-id="26dd4-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="26dd4-107">**ulSize**</span></span>
  
> <span data-ttu-id="26dd4-108">構造体のサイズ。</span><span class="sxs-lookup"><span data-stu-id="26dd4-108">The size of the structure.</span></span>
    
 <span data-ttu-id="26dd4-109">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="26dd4-109">**ulFlags**</span></span>
  
> <span data-ttu-id="26dd4-110">同期の種類を示すフラグ。これは、次のいずれかの値である必要があります。</span><span class="sxs-lookup"><span data-stu-id="26dd4-110">A flag that indicates the type of sync. It must be one of the following values:</span></span>
    
||||
|:-----|:-----|:-----|
|<span data-ttu-id="26dd4-111">SYNC_OUTGOING_MAIL</span><span class="sxs-lookup"><span data-stu-id="26dd4-111">SYNC_OUTGOING_MAIL</span></span>  <br/> |<span data-ttu-id="26dd4-112">0x00000200</span><span class="sxs-lookup"><span data-stu-id="26dd4-112">0x00000200</span></span>  <br/> |<span data-ttu-id="26dd4-113">(現在使用されていない) サーバーにメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="26dd4-113">Send the message to the server (not currently in use).</span></span>  <br/> |
|<span data-ttu-id="26dd4-114">SYNC_UPLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="26dd4-114">SYNC_UPLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="26dd4-115">0x00000001</span><span class="sxs-lookup"><span data-stu-id="26dd4-115">0x00000001</span></span>  <br/> |<span data-ttu-id="26dd4-116">階層の変更をサーバーにプッシュします。</span><span class="sxs-lookup"><span data-stu-id="26dd4-116">Push hierarchy changes to the server.</span></span>  <br/> |
|<span data-ttu-id="26dd4-117">SYNC_DOWNLOAD_HIERARCHY</span><span class="sxs-lookup"><span data-stu-id="26dd4-117">SYNC_DOWNLOAD_HIERARCHY</span></span>  <br/> |<span data-ttu-id="26dd4-118">0x00000002</span><span class="sxs-lookup"><span data-stu-id="26dd4-118">0x00000002</span></span>  <br/> |<span data-ttu-id="26dd4-119">階層の変更をサーバーからプルします。</span><span class="sxs-lookup"><span data-stu-id="26dd4-119">Pull hierarchy changes from server.</span></span>  <br/> |
|<span data-ttu-id="26dd4-120">SYNC_UPLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="26dd4-120">SYNC_UPLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="26dd4-121">0x00000040</span><span class="sxs-lookup"><span data-stu-id="26dd4-121">0x00000040</span></span>  <br/> |<span data-ttu-id="26dd4-122">メッセージの変更をサーバーにプッシュします。</span><span class="sxs-lookup"><span data-stu-id="26dd4-122">Push message changes to server.</span></span>  <br/> |
|<span data-ttu-id="26dd4-123">SYNC_DOWNLOAD_CONTENTS</span><span class="sxs-lookup"><span data-stu-id="26dd4-123">SYNC_DOWNLOAD_CONTENTS</span></span>  <br/> |<span data-ttu-id="26dd4-124">0x00000080</span><span class="sxs-lookup"><span data-stu-id="26dd4-124">0x00000080</span></span>  <br/> |<span data-ttu-id="26dd4-125">サーバーからメッセージの変更をプルします。</span><span class="sxs-lookup"><span data-stu-id="26dd4-125">Pull message changes from server.</span></span>  <br/> |
|<span data-ttu-id="26dd4-126">SYNC_ON_DEMAND</span><span class="sxs-lookup"><span data-stu-id="26dd4-126">SYNC_ON_DEMAND</span></span>  <br/> |<span data-ttu-id="26dd4-127">0x20000000</span><span class="sxs-lookup"><span data-stu-id="26dd4-127">0x20000000</span></span>  <br/> |<span data-ttu-id="26dd4-128">同期はユーザーによって開始され、優先度が高い必要があります。</span><span class="sxs-lookup"><span data-stu-id="26dd4-128">The sync was initiated by the user and should be a higher priority.</span></span>  <br/> |
|<span data-ttu-id="26dd4-129">SYNC_GLOBAL_HEADERS</span><span class="sxs-lookup"><span data-stu-id="26dd4-129">SYNC_GLOBAL_HEADERS</span></span>  <br/> |<span data-ttu-id="26dd4-130">0x02000000</span><span class="sxs-lookup"><span data-stu-id="26dd4-130">0x02000000</span></span>  <br/> |<span data-ttu-id="26dd4-131">ヘッダーのみを同期し、完全なボディを同期しない必要があります。</span><span class="sxs-lookup"><span data-stu-id="26dd4-131">Should only sync headers and not full bodies.</span></span>  <br/> |
   
 <span data-ttu-id="26dd4-132">**psesSync**</span><span class="sxs-lookup"><span data-stu-id="26dd4-132">**psesSync**</span></span>
  
> <span data-ttu-id="26dd4-133">[IN]MAPI セッションへのポインター。</span><span class="sxs-lookup"><span data-stu-id="26dd4-133">[IN] A pointer to the MAPI session.</span></span>
    
 <span data-ttu-id="26dd4-134">**punkCallBack**</span><span class="sxs-lookup"><span data-stu-id="26dd4-134">**punkCallBack**</span></span>
  
> <span data-ttu-id="26dd4-135">[IN]進行状況を提供するインターフェイスへのポインター。</span><span class="sxs-lookup"><span data-stu-id="26dd4-135">[IN] A pointer to the interface on which to provide progress.</span></span> <span data-ttu-id="26dd4-136">[IMAPISyncProgressCallback : IUnknown のインターフェイスを照会するために使用できます](imapisyncprogresscallbackiunknown.md)。</span><span class="sxs-lookup"><span data-stu-id="26dd4-136">It can be used to query the interface for [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md).</span></span>
    
 <span data-ttu-id="26dd4-137">**\*phSyncDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="26dd4-137">**\*phSyncDoneEvent**</span></span>
  
> <span data-ttu-id="26dd4-138">[OUT]作成されたスレッドが完了した場合に発生するイベント。</span><span class="sxs-lookup"><span data-stu-id="26dd4-138">[OUT] The event that will occur when the thread that was just created is complete.</span></span> <span data-ttu-id="26dd4-139">ポインターはイベントを含むので有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="26dd4-139">The pointer must be valid because it will contain the event.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26dd4-140">関連項目</span><span class="sxs-lookup"><span data-stu-id="26dd4-140">See also</span></span>



[<span data-ttu-id="26dd4-141">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26dd4-141">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)
  
[<span data-ttu-id="26dd4-142">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26dd4-142">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)

