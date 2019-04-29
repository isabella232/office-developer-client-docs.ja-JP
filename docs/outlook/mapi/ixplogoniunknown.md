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
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 46f4e3fc8f554f332ab9b1d8a6cb33e9e21dd9a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432535"
---
# <a name="ixplogon--iunknown"></a><span data-ttu-id="eb732-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb732-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="eb732-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb732-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb732-105">トランスポートプロバイダーへの MAPI スプーラーアクセスを提供します。</span><span class="sxs-lookup"><span data-stu-id="eb732-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb732-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="eb732-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb732-107">Mapispi</span><span class="sxs-lookup"><span data-stu-id="eb732-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="eb732-108">公開者:</span><span class="sxs-lookup"><span data-stu-id="eb732-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="eb732-109">トランスポートログオンオブジェクト</span><span class="sxs-lookup"><span data-stu-id="eb732-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="eb732-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="eb732-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb732-111">トランスポートプロバイダー</span><span class="sxs-lookup"><span data-stu-id="eb732-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="eb732-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="eb732-112">Called by:</span></span>  <br/> |<span data-ttu-id="eb732-113">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="eb732-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="eb732-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="eb732-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="eb732-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="eb732-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="eb732-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="eb732-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="eb732-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="eb732-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="eb732-118">v の順序</span><span class="sxs-lookup"><span data-stu-id="eb732-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="eb732-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="eb732-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="eb732-120">トランスポートプロバイダーが処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="eb732-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="eb732-121">**registeroptions**</span><span class="sxs-lookup"><span data-stu-id="eb732-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="eb732-122">*サポートされていないか文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="eb732-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="eb732-123">transportnotify</span><span class="sxs-lookup"><span data-stu-id="eb732-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="eb732-124">トランスポートプロバイダーが通知を要求したイベントが発生したことを通知します。</span><span class="sxs-lookup"><span data-stu-id="eb732-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="eb732-125">アイドル</span><span class="sxs-lookup"><span data-stu-id="eb732-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="eb732-126">システムがアイドル状態であることを示します。これにより、トランスポートプロバイダーは優先度の低い操作を実行できるようになります。</span><span class="sxs-lookup"><span data-stu-id="eb732-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="eb732-127">transportlogoff</span><span class="sxs-lookup"><span data-stu-id="eb732-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="eb732-128">ログオフプロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="eb732-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="eb732-129">submitmessage</span><span class="sxs-lookup"><span data-stu-id="eb732-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="eb732-130">トランスポートプロバイダーが配信するメッセージを MAPI スプーラーに指定します。</span><span class="sxs-lookup"><span data-stu-id="eb732-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="eb732-131">endmessage</span><span class="sxs-lookup"><span data-stu-id="eb732-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="eb732-132">MAPI スプーラーが送信メッセージの処理を完了したことをトランスポートプロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="eb732-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="eb732-133">間隔</span><span class="sxs-lookup"><span data-stu-id="eb732-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="eb732-134">トランスポートプロバイダーが1つ以上の受信メッセージを受信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="eb732-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="eb732-135">startmessage</span><span class="sxs-lookup"><span data-stu-id="eb732-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="eb732-136">トランスポートプロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="eb732-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="eb732-137">openstatusentry</span><span class="sxs-lookup"><span data-stu-id="eb732-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="eb732-138">トランスポートプロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="eb732-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="eb732-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="eb732-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="eb732-140">トランスポートプロバイダーの外部の状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="eb732-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="eb732-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="eb732-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="eb732-142">保留中の受信または送信メッセージをすべてトランスポートプロバイダーが直ちに配信するよう要求します。</span><span class="sxs-lookup"><span data-stu-id="eb732-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="eb732-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="eb732-143">See also</span></span>



[<span data-ttu-id="eb732-144">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="eb732-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

