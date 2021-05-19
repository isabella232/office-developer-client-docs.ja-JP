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
# <a name="ixplogon--iunknown"></a><span data-ttu-id="1e3d6-103">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e3d6-103">IXPLogon : IUnknown</span></span>

  
  
<span data-ttu-id="1e3d6-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e3d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e3d6-105">MAPI スプーラーにトランスポート プロバイダーへのアクセス権を与えます。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-105">Gives the MAPI spooler access to a transport provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1e3d6-106">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="1e3d6-106">Header file:</span></span>  <br/> |<span data-ttu-id="1e3d6-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="1e3d6-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="1e3d6-108">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1e3d6-109">トランスポート ログオン オブジェクト</span><span class="sxs-lookup"><span data-stu-id="1e3d6-109">Transport logon objects</span></span>  <br/> |
|<span data-ttu-id="1e3d6-110">実装元:</span><span class="sxs-lookup"><span data-stu-id="1e3d6-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1e3d6-111">トランスポート プロバイダー</span><span class="sxs-lookup"><span data-stu-id="1e3d6-111">Transport providers</span></span>  <br/> |
|<span data-ttu-id="1e3d6-112">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="1e3d6-112">Called by:</span></span>  <br/> |<span data-ttu-id="1e3d6-113">MAPI スプーラー</span><span class="sxs-lookup"><span data-stu-id="1e3d6-113">The MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="1e3d6-114">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="1e3d6-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1e3d6-115">IID_IXPLogon</span><span class="sxs-lookup"><span data-stu-id="1e3d6-115">IID_IXPLogon</span></span>  <br/> |
|<span data-ttu-id="1e3d6-116">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="1e3d6-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1e3d6-117">LXPLOGON</span><span class="sxs-lookup"><span data-stu-id="1e3d6-117">LXPLOGON</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1e3d6-118">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="1e3d6-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1e3d6-119">AddressTypes</span><span class="sxs-lookup"><span data-stu-id="1e3d6-119">AddressTypes</span></span>](ixplogon-addresstypes.md) <br/> |<span data-ttu-id="1e3d6-120">トランスポート プロバイダーが処理する受信者の種類を返します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-120">Returns the types of recipients that the transport provider handles.</span></span>  <br/> |
|<span data-ttu-id="1e3d6-121">**RegisterOptions**</span><span class="sxs-lookup"><span data-stu-id="1e3d6-121">**RegisterOptions**</span></span> <br/> | <span data-ttu-id="1e3d6-122">*サポートされていないか、文書化されていません。*</span><span class="sxs-lookup"><span data-stu-id="1e3d6-122">*Not supported or documented.*</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-123">TransportNotify</span><span class="sxs-lookup"><span data-stu-id="1e3d6-123">TransportNotify</span></span>](ixplogon-transportnotify.md) <br/> |<span data-ttu-id="1e3d6-124">トランスポート プロバイダーが通知を要求したイベントの発生を通知します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-124">Signals the occurrence of an event about which the transport provider requested notification.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-125">アイドル状態</span><span class="sxs-lookup"><span data-stu-id="1e3d6-125">Idle</span></span>](ixplogon-idle.md) <br/> |<span data-ttu-id="1e3d6-126">システムがアイドル状態で、トランスポート プロバイダーが優先度の低い操作を実行できる状態を示します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-126">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-127">TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="1e3d6-127">TransportLogoff</span></span>](ixplogon-transportlogoff.md) <br/> |<span data-ttu-id="1e3d6-128">ログオフ プロセスを開始します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-128">Initiates the logoff process.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-129">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="1e3d6-129">SubmitMessage</span></span>](ixplogon-submitmessage.md) <br/> |<span data-ttu-id="1e3d6-130">MAPI スプーラーにトランスポート プロバイダーが配信するメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-130">Indicates that the MAPI spooler has a message for the transport provider to deliver.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-131">EndMessage</span><span class="sxs-lookup"><span data-stu-id="1e3d6-131">EndMessage</span></span>](ixplogon-endmessage.md) <br/> |<span data-ttu-id="1e3d6-132">MAPI スプーラーが送信メッセージの処理を完了したとトランスポート プロバイダーに通知します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-132">Informs the transport provider that the MAPI spooler completed its processing on an outbound message.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-133">Poll</span><span class="sxs-lookup"><span data-stu-id="1e3d6-133">Poll</span></span>](ixplogon-poll.md) <br/> |<span data-ttu-id="1e3d6-134">トランスポート プロバイダーが 1 つ以上の受信メッセージを受信したかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-134">Indicates whether the transport provider has received one or more inbound messages.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-135">StartMessage</span><span class="sxs-lookup"><span data-stu-id="1e3d6-135">StartMessage</span></span>](ixplogon-startmessage.md) <br/> |<span data-ttu-id="1e3d6-136">トランスポート プロバイダーから MAPI スプーラーへの受信メッセージの転送を開始します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-136">Initiates the transfer of an inbound message from the transport provider to the MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-137">OpenStatusEntry</span><span class="sxs-lookup"><span data-stu-id="1e3d6-137">OpenStatusEntry</span></span>](ixplogon-openstatusentry.md) <br/> |<span data-ttu-id="1e3d6-138">トランスポート プロバイダーの状態オブジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-138">Opens the transport provider's status object.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-139">ValidateState</span><span class="sxs-lookup"><span data-stu-id="1e3d6-139">ValidateState</span></span>](ixplogon-validatestate.md) <br/> |<span data-ttu-id="1e3d6-140">トランスポート プロバイダーの外部状態を確認します。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-140">Checks the transport provider's external status.</span></span>  <br/> |
|[<span data-ttu-id="1e3d6-141">FlushQueues</span><span class="sxs-lookup"><span data-stu-id="1e3d6-141">FlushQueues</span></span>](ixplogon-flushqueues.md) <br/> |<span data-ttu-id="1e3d6-142">トランスポート プロバイダーが保留中のすべての受信メッセージまたは送信メッセージを直ちに配信する要求。</span><span class="sxs-lookup"><span data-stu-id="1e3d6-142">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e3d6-143">関連項目</span><span class="sxs-lookup"><span data-stu-id="1e3d6-143">See also</span></span>



[<span data-ttu-id="1e3d6-144">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="1e3d6-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

