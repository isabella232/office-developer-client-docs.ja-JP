---
title: IXPLogon IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon
api_type:
- COM
ms.assetid: 4d24ecaf-11d0-4362-8207-be3407736d7b
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282797"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="e9dd2-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e9dd2-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="e9dd2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9dd2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9dd2-105">トランスポートプロバイダーへの MAPI スプーラーアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9dd2-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="e9dd2-106">Header file:</span></span>  <br/> |<span data-ttu-id="e9dd2-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="e9dd2-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e9dd2-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="e9dd2-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="e9dd2-109">トランスポートログオンオブジェクト</span><span class="sxs-lookup"><span data-stu-id="e9dd2-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="e9dd2-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="e9dd2-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="e9dd2-111">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="e9dd2-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="e9dd2-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="e9dd2-112">Called by:</span></span>  <br/> |<span data-ttu-id="e9dd2-113">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="e9dd2-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="e9dd2-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="e9dd2-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e9dd2-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="e9dd2-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="e9dd2-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="e9dd2-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="e9dd2-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="e9dd2-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e9dd2-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="e9dd2-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e9dd2-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="e9dd2-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="e9dd2-120">トランスポートプロバイダーが処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="e9dd2-121">**registeroptions**</span><span class="sxs-lookup"><span data-stu-id="e9dd2-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="e9dd2-122">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="e9dd2-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-123">transportnotify</span><span class="sxs-lookup"><span data-stu-id="e9dd2-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="e9dd2-124">トランスポートプロバイダーが通知を要求したイベントが発生したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-125">アイドル</span><span class="sxs-lookup"><span data-stu-id="e9dd2-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="e9dd2-126">システムがアイドル状態であることを示します。これにより、トランスポートプロバイダーは優先度の低い操作を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-127">transportlogoff</span><span class="sxs-lookup"><span data-stu-id="e9dd2-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="e9dd2-128">ログオフプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-129">submitmessage</span><span class="sxs-lookup"><span data-stu-id="e9dd2-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="e9dd2-130">トランスポートプロバイダーが配信するメッセージを MAPI スプーラーに指定します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-131">endmessage</span><span class="sxs-lookup"><span data-stu-id="e9dd2-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="e9dd2-132">MAPI スプーラーが送信メッセージの処理を完了したことをトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-133">間隔</span><span class="sxs-lookup"><span data-stu-id="e9dd2-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="e9dd2-134">トランスポートプロバイダーが1つ以上の受信メッセージを受信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-135">startmessage</span><span class="sxs-lookup"><span data-stu-id="e9dd2-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="e9dd2-136">トランスポートプロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-137">openstatusentry</span><span class="sxs-lookup"><span data-stu-id="e9dd2-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="e9dd2-138">トランスポートプロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="e9dd2-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="e9dd2-140">トランスポートプロバイダーの外部の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="e9dd2-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e9dd2-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="e9dd2-142">保留中の受信または送信メッセージをすべてトランスポートプロバイダーが直ちに配信するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="e9dd2-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e9dd2-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9dd2-143">See also</span></span>



[<span data-ttu-id="e9dd2-144">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="e9dd2-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

