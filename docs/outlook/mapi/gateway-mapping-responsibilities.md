---
title: ゲートウェイのマッピング責任
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422755"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="bb5d0-103">ゲートウェイのマッピング責任</span><span class="sxs-lookup"><span data-stu-id="bb5d0-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="bb5d0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb5d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb5d0-105">MAPI 対応ゲートウェイが、ゲートウェイマップ可能なプロパティを含む特別なプロパティ セットの 1 つで名前付きプロパティを含むメッセージを受信すると、ゲートウェイは、すべてのプロパティを宛先メッセージング システムのプロトコルにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="bb5d0-106">MAPI では、ゲートウェイが特別なプロパティ セット内のすべての名前付きプロパティを処理する方法をお勧めしますが、ゲートウェイは、電子メール アドレスとアドレスの種類の 2 つのみを処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="bb5d0-107">電子メール アドレスとアドレスの種類のプロパティはメッセージの送信に直接影響を与えるので、ゲートウェイがこれら 2 つのプロパティのマッピングをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="bb5d0-108">検索キーはユーザーのアドレスの種類とアドレスで構成されるので、可能な限り翻訳する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="bb5d0-109">エントリ識別子は頻繁に処理されません。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="bb5d0-110">あるメッセージング システムから別のメッセージング システムで使用できるエントリ識別子へのエントリ識別子のマッピングを有効にするには、ゲートウェイが両方のシステムの形式を使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="bb5d0-111">ほとんどのゲートウェイはエントリ識別子の形式を認識しないので、エントリ識別子の変換はまれです。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="bb5d0-112">頻繁に変換されないマップ可能なプロパティの 1 つが表示名です。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="bb5d0-113">ゲートウェイは、表示名を保存して送信する必要がありますが、必ずしも変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="bb5d0-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

