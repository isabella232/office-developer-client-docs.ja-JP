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
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: 1803707b46b9b58e7372e7e58cc36241d0ebdb4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571725"
---
# <a name="itnef--iunknown"></a><span data-ttu-id="7d04e-103">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7d04e-103">ITnef : IUnknown</span></span>

  
  
<span data-ttu-id="7d04e-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d04e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d04e-105">メッセージに関連付けることができるバイナリ ストリームに、メッセージング システムがサポートされていない MAPI プロパティをカプセル化するためのメソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="7d04e-105">Provides methods for encapsulating MAPI properties that are not supported by a messaging system into binary streams that can be attached to messages.</span></span> <span data-ttu-id="7d04e-106">このカプセル化に使用される形式は、トランスポート ニュートラル カプセル化形式 (TNEF) です。</span><span class="sxs-lookup"><span data-stu-id="7d04e-106">The format used for this encapsulation is the Transport-Neutral Encapsulation Format (TNEF).</span></span> <span data-ttu-id="7d04e-107">ターゲット トランスポート プロバイダーまたは MAPI ベースのクライアント アプリケーション、TNEF の添付ファイルを含むメッセージを受信するには、回復できます、プロパティ、添付ファイルから。</span><span class="sxs-lookup"><span data-stu-id="7d04e-107">The target transport provider or MAPI-based client application can then, on receiving a message that includes a TNEF attachment, recover the properties from the attachment.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7d04e-108">ヘッダー ファイル:</span><span class="sxs-lookup"><span data-stu-id="7d04e-108">Header file:</span></span>  <br/> |<span data-ttu-id="7d04e-109">Tnef.h</span><span class="sxs-lookup"><span data-stu-id="7d04e-109">Tnef.h</span></span>  <br/> |
|<span data-ttu-id="7d04e-110">によって公開されます。</span><span class="sxs-lookup"><span data-stu-id="7d04e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="7d04e-111">TNEF オブジェクト</span><span class="sxs-lookup"><span data-stu-id="7d04e-111">TNEF objects</span></span>  <br/> |
|<span data-ttu-id="7d04e-112">によって実装されます。</span><span class="sxs-lookup"><span data-stu-id="7d04e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="7d04e-113">MAPI</span><span class="sxs-lookup"><span data-stu-id="7d04e-113">MAPI</span></span>  <br/> |
|<span data-ttu-id="7d04e-114">によって呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="7d04e-114">Called by:</span></span>  <br/> |<span data-ttu-id="7d04e-115">トランスポート プロバイダー、メッセージ ストア プロバイダー、およびゲートウェイ</span><span class="sxs-lookup"><span data-stu-id="7d04e-115">Transport providers, message store providers, and gateways</span></span>  <br/> |
|<span data-ttu-id="7d04e-116">インターフェイスの識別子。</span><span class="sxs-lookup"><span data-stu-id="7d04e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7d04e-117">IID_ITNEF</span><span class="sxs-lookup"><span data-stu-id="7d04e-117">IID_ITNEF</span></span>  <br/> |
|<span data-ttu-id="7d04e-118">ポインターの型。</span><span class="sxs-lookup"><span data-stu-id="7d04e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="7d04e-119">LPTNEF</span><span class="sxs-lookup"><span data-stu-id="7d04e-119">LPTNEF</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7d04e-120">Vtable の順序</span><span class="sxs-lookup"><span data-stu-id="7d04e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7d04e-121">AddProps</span><span class="sxs-lookup"><span data-stu-id="7d04e-121">AddProps</span></span>](itnef-addprops.md) <br/> |<span data-ttu-id="7d04e-122">メッセージまたは添付ファイルをカプセル化するプロパティを追加するのには、呼び出し元のサービス プロバイダーまたはゲートウェイを有効にします。</span><span class="sxs-lookup"><span data-stu-id="7d04e-122">Enables the calling service provider or gateway to add properties to the encapsulation of a message or an attachment.</span></span>  <br/> |
|[<span data-ttu-id="7d04e-123">ExtractProps</span><span class="sxs-lookup"><span data-stu-id="7d04e-123">ExtractProps</span></span>](itnef-extractprops.md) <br/> |<span data-ttu-id="7d04e-124">TNEF のカプセル化のプロパティを抽出します。</span><span class="sxs-lookup"><span data-stu-id="7d04e-124">Extracts the properties from a TNEF encapsulation.</span></span>  <br/> |
|[<span data-ttu-id="7d04e-125">Finish</span><span class="sxs-lookup"><span data-stu-id="7d04e-125">Finish</span></span>](itnef-finish.md) <br/> |<span data-ttu-id="7d04e-126">完了するとキューに登録されたすべての TNEF の操作を処理し、待機しています。</span><span class="sxs-lookup"><span data-stu-id="7d04e-126">Finishes processing for all TNEF operations that are queued and waiting.</span></span>  <br/> |
|[<span data-ttu-id="7d04e-127">OpenTaggedBody</span><span class="sxs-lookup"><span data-stu-id="7d04e-127">OpenTaggedBody</span></span>](itnef-opentaggedbody.md) <br/> |<span data-ttu-id="7d04e-128">カプセル化されたメッセージのテキストのストリームのインタ フェースを開きます。</span><span class="sxs-lookup"><span data-stu-id="7d04e-128">Opens a stream interface on the text of an encapsulated message.</span></span>  <br/> |
|[<span data-ttu-id="7d04e-129">SetProps</span><span class="sxs-lookup"><span data-stu-id="7d04e-129">SetProps</span></span>](itnef-setprops.md) <br/> |<span data-ttu-id="7d04e-130">元のメッセージまたは添付ファイルを変更することがなくカプセル化されたメッセージまたは添付ファイルの 1 つまたは複数のプロパティの値を設定します。</span><span class="sxs-lookup"><span data-stu-id="7d04e-130">Sets the value of one or more properties for an encapsulated message or attachment without modifying the original message or attachment.</span></span>  <br/> |
|[<span data-ttu-id="7d04e-131">EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="7d04e-131">EncodeRecips</span></span>](itnef-encoderecips.md) <br/> |<span data-ttu-id="7d04e-132">メッセージの TNEF データ ストリーム内のメッセージの受信者テーブルのビューをエンコードします。</span><span class="sxs-lookup"><span data-stu-id="7d04e-132">Encodes a view for a message's recipient table in the TNEF data stream for the message.</span></span>  <br/> |
|[<span data-ttu-id="7d04e-133">FinishComponent</span><span class="sxs-lookup"><span data-stu-id="7d04e-133">FinishComponent</span></span>](itnef-finishcomponent.md) <br/> |<span data-ttu-id="7d04e-134">TNEF ストリームに同時に 1 つのメッセージからの個々 のコンポーネントを処理します。</span><span class="sxs-lookup"><span data-stu-id="7d04e-134">Processes individual components from a message one at a time into a TNEF stream.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7d04e-135">関連項目</span><span class="sxs-lookup"><span data-stu-id="7d04e-135">See also</span></span>



[<span data-ttu-id="7d04e-136">MAPI インターフェイス</span><span class="sxs-lookup"><span data-stu-id="7d04e-136">MAPI Interfaces</span></span>](mapi-interfaces.md)

