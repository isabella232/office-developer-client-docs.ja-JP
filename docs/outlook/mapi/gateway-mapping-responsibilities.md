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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342799"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="277b7-103">ゲートウェイのマッピング責任</span><span class="sxs-lookup"><span data-stu-id="277b7-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="277b7-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="277b7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="277b7-105">ゲートウェイマップ可能プロパティを格納するように指定された特別なプロパティセットのいずれかで、MAPI 対応ゲートウェイが名前付きプロパティを含むメッセージを受信すると、ゲートウェイは、すべてのプロパティを送信先メッセージングシステムのプロトコルにマップする必要があります。</span><span class="sxs-lookup"><span data-stu-id="277b7-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="277b7-106">MAPI では、特別なプロパティセット内のすべての名前付きプロパティをゲートウェイで処理することをお勧めしますが、ゲートウェイは、電子メールアドレスとアドレスの種類が2つだけ処理されることを想定しています。</span><span class="sxs-lookup"><span data-stu-id="277b7-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="277b7-107">電子メールアドレスおよびアドレスの種類のプロパティは、メッセージの送信に直接影響するため、ゲートウェイがこれら2つのプロパティのマッピングをサポートすることが重要です。</span><span class="sxs-lookup"><span data-stu-id="277b7-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="277b7-108">検索キーはユーザーのアドレスの種類と住所で構成されるため、可能な場合は、それらも翻訳する必要があります。</span><span class="sxs-lookup"><span data-stu-id="277b7-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="277b7-109">エントリ識別子が頻繁に処理されることは想定されていません。</span><span class="sxs-lookup"><span data-stu-id="277b7-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="277b7-110">あるメッセージングシステムで使用されているエントリ識別子から、別のメッセージングシステムで使用可能なエントリ id へのマッピングを有効にするには、ゲートウェイが両方のシステムの形式を使用できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="277b7-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="277b7-111">ほとんどのゲートウェイはエントリ識別子の形式を認識していないため、エントリ識別子の変換はめったにありません。</span><span class="sxs-lookup"><span data-stu-id="277b7-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="277b7-112">頻繁に変換することが想定されていない別のマッピング可能なプロパティが表示名です。</span><span class="sxs-lookup"><span data-stu-id="277b7-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="277b7-113">ゲートウェイは、表示名を格納して送信する必要がありますが、必ずしも変換する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="277b7-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

