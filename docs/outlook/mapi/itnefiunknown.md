---
title: ITnef IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef
api_type:
- COM
ms.assetid: eddca896-9497-4425-9904-87ef3cbae298
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 1f815a914deb5e21f3d913abe46a84cc7a32b4ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428516"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="c1de0-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c1de0-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="c1de0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1de0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1de0-105">メッセージング システムでサポートされていない MAPI プロパティを、メッセージに接続できるバイナリ ストリームにカプセル化するメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="c1de0-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="c1de0-106">このカプセル化に使用される形式は、Transport-Neutralカプセル化形式 (TNEF) です。</span><span class="sxs-lookup"><span data-stu-id="c1de0-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="c1de0-107">ターゲット トランスポート プロバイダーまたは MAPI ベースのクライアント アプリケーションは、TNEF 添付ファイルを含むメッセージを受信すると、添付ファイルからプロパティを回復できます。</span><span class="sxs-lookup"><span data-stu-id="c1de0-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c1de0-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="c1de0-108">Header file:</span></span>  <br/> |<span data-ttu-id="c1de0-109">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="c1de0-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="c1de0-110">次のユーザーによって公開されます。</span><span class="sxs-lookup"><span data-stu-id="c1de0-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="c1de0-111">TNEF オブジェクト</span><span class="sxs-lookup"><span data-stu-id="c1de0-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="c1de0-112">実装元:</span><span class="sxs-lookup"><span data-stu-id="c1de0-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="c1de0-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="c1de0-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="c1de0-114">呼び出し元:</span><span class="sxs-lookup"><span data-stu-id="c1de0-114">Called by:</span></span>  <br/> |<span data-ttu-id="c1de0-115">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="c1de0-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="c1de0-116">インターフェイス識別子:</span><span class="sxs-lookup"><span data-stu-id="c1de0-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="c1de0-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="c1de0-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="c1de0-118">ポインターの種類:</span><span class="sxs-lookup"><span data-stu-id="c1de0-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="c1de0-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="c1de0-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="c1de0-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="c1de0-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="c1de0-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="c1de0-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="c1de0-122">呼び出し元のサービス プロバイダーまたはゲートウェイが、メッセージまたは添付ファイルのカプセル化にプロパティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c1de0-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="c1de0-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="c1de0-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="c1de0-124">TNEF カプセル化からプロパティを抽出します。</span><span class="sxs-lookup"><span data-stu-id="c1de0-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="c1de0-125">Finish</span><span class="sxs-lookup"><span data-stu-id="c1de0-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="c1de0-126">キューに入れ、待機しているすべての TNEF 操作の処理を終了します。</span><span class="sxs-lookup"><span data-stu-id="c1de0-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="c1de0-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="c1de0-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="c1de0-128">カプセル化されたメッセージのテキストにストリーム インターフェイスを開きます。</span><span class="sxs-lookup"><span data-stu-id="c1de0-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="c1de0-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="c1de0-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="c1de0-130">元のメッセージまたは添付ファイルを変更せずに、カプセル化されたメッセージまたは添付ファイルの 1 つ以上のプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="c1de0-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="c1de0-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="c1de0-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="c1de0-132">メッセージの TNEF データ ストリーム内のメッセージの受信者テーブルのビューをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="c1de0-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="c1de0-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="c1de0-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="c1de0-134">メッセージの個々のコンポーネントを一度に 1 つの TNEF ストリームに処理します。</span><span class="sxs-lookup"><span data-stu-id="c1de0-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1de0-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="c1de0-135">See also</span></span>



[<span data-ttu-id="c1de0-136">MAPI のインターフェイス</span><span class="sxs-lookup"><span data-stu-id="c1de0-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

