---
title: ゲートウェイ マッピングの責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 91c1d9293108b96fde43b769c97ec673f82a8cb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563031"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="e4f0c-103">ゲートウェイ マッピングの責任</span><span class="sxs-lookup"><span data-stu-id="e4f0c-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="e4f0c-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e4f0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e4f0c-105">MAPI 対応のゲートウェイは、ゲートウェイのマッピングが可能なプロパティを持つように指定された特別なプロパティ セットの 1 つの名前付きプロパティを含むメッセージを受信するときにゲートウェイする必要がありますすべてのプロパティにマップ リンク先のメッセージング システムのプロトコル。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="e4f0c-106">ゲートウェイが 2 つだけを処理するために期待されるが、MAPI では、ゲートウェイが、特別なプロパティ セット内のすべての名前付きプロパティを処理することをお勧め、: 電子メール アドレス、アドレスの種類です。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="e4f0c-107">電子メール アドレスとアドレスの種類のプロパティは、メッセージの送信に直接影響、ために、ゲートウェイがこれら 2 つのプロパティのマッピングをサポートすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="e4f0c-108">検索キーは、ユーザーのアドレスの種類とアドレスで構成されています、ためにを可能であれば、変換することもか。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="e4f0c-109">エントリ id を頻繁に処理する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="e4f0c-110">ゲートウェイは、別のメッセージング システムで使用可能なエントリの識別子を 1 つのメッセージング システムで生成されたエントリの識別子のマッピングを有効にするには、両方のシステムの形式を使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="e4f0c-111">ほとんどのゲートウェイがエントリの識別子の形式を認識できないため、エントリの識別子の翻訳はほとんどありません。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="e4f0c-112">頻繁に変換するのには予期しない別のマッピング可能なプロパティは、表示名です。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="e4f0c-113">ゲートウェイ必要があります表示名を格納したり、転送が、必ずしもそれらを変換します。</span><span class="sxs-lookup"><span data-stu-id="e4f0c-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

