---
title: メッセージング ドメイン間での送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410113"
---
# <a name="sending-across-messaging-domains"></a><span data-ttu-id="cccaf-103">メッセージング ドメイン間での送信</span><span class="sxs-lookup"><span data-stu-id="cccaf-103">Sending Across Messaging Domains</span></span>

  
  
<span data-ttu-id="cccaf-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cccaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cccaf-105">メッセージング ドメインは、共通のアドレス形式を共有する 1 つ以上のメッセージング システムを表します。</span><span class="sxs-lookup"><span data-stu-id="cccaf-105">A messaging domain represents one or more messaging systems that share a common address format.</span></span> <span data-ttu-id="cccaf-106">複数のメッセージング ドメイン間の通信では、元のメッセージング ドメインの形式で送信されたメッセージを宛先メッセージング ドメインの形式に変換します。</span><span class="sxs-lookup"><span data-stu-id="cccaf-106">Communication across multiple messaging domains involves translating a message sent in the format of the original messaging domain into the format of the destination messaging domain.</span></span> <span data-ttu-id="cccaf-107">すべてのアドレス形式に互換性がある訳ではないので、宛先形式にアドレス情報を変換するゲートウェイが必要です。</span><span class="sxs-lookup"><span data-stu-id="cccaf-107">Because not all address formats are compatible, a gateway is needed to translate the addressing information from the source format into the destination format.</span></span> <span data-ttu-id="cccaf-108">メッセージング ドメイン全体の有効性を確保するために、クライアント アプリケーションは MAPI プロパティに重要なアドレス情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="cccaf-108">To ensure validity across messaging domains, client applications store important addressing information in MAPI properties.</span></span> <span data-ttu-id="cccaf-109">さらに、ゲートウェイは変換を実行し、変換が必要と知られているプロパティを調べ、変換先メッセージング ドメインが使用できる形式に変更します。</span><span class="sxs-lookup"><span data-stu-id="cccaf-109">In addition, gateways perform the translation, examining the properties known to need translation and changing them to a format that the destination messaging domain can use.</span></span>
  
<span data-ttu-id="cccaf-110">以前は、MAPI では、このアドレス指定情報をメッセージの現在の受信者リストを構成するユーザーにのみ関連付けがありました。</span><span class="sxs-lookup"><span data-stu-id="cccaf-110">Previously, MAPI allowed this addressing information to be associated with only the users who comprise a message's current recipient list.</span></span> <span data-ttu-id="cccaf-111">受信者リストの各メンバーを記述するプロパティは、メッセージング ドメイン間の有効性を確保するためにゲートウェイによって必要な変換を受け取った。</span><span class="sxs-lookup"><span data-stu-id="cccaf-111">The properties describing each member of the recipient list underwent the required translation by the gateway to ensure validity across messaging domains.</span></span> <span data-ttu-id="cccaf-112">ただし、一部のアプリケーションでは、メッセージに、過去に受信者だった、将来受信者になる、または受信者にはならないユーザーに関するアドレス指定情報が含まれる必要があります。</span><span class="sxs-lookup"><span data-stu-id="cccaf-112">However, some applications require that their messages include addressing information about users that perhaps were recipients in the past, will be recipients in the future, or will never be recipients.</span></span> <span data-ttu-id="cccaf-113">たとえば、ユーザーのグループに指定された順序でメッセージを送信するルーティング アプリケーションは、これらのユーザーに関するアドレス情報をメッセージに埋め込む。</span><span class="sxs-lookup"><span data-stu-id="cccaf-113">For example, routing applications, which send messages in a specified order to a group of users, embed addressing information about these users in the messages.</span></span> <span data-ttu-id="cccaf-114">埋め込み情報には、通常、将来の受信者のアドレスとアドレスの種類、およびルーティング順序での役割と位置、その名前、および受信者ごとの 1 つ以上のバイナリ識別子が含まれます。</span><span class="sxs-lookup"><span data-stu-id="cccaf-114">The embedded information typically includes the address and address type of the future recipients, and perhaps also their roles and positions in the routing order, their names, and one or more binary identifiers per recipient.</span></span>
  
<span data-ttu-id="cccaf-115">これらの非重要なユーザーに関する情報をメッセージに含めるには、MAPI には、この重要でない情報がメッセージング ドメイン間でも正しく変換されるようにするための戦略が含まれています。</span><span class="sxs-lookup"><span data-stu-id="cccaf-115">To enable messages to include information about these nonrecipient users, MAPI now includes a strategy for ensuring that this nonrecipient information is also translated correctly across messaging domains.</span></span> <span data-ttu-id="cccaf-116">この戦略は、ゲートウェイマップ可能なプロパティの概念に基づいて行います。</span><span class="sxs-lookup"><span data-stu-id="cccaf-116">This strategy is based on the concept of gateway-mappable properties.</span></span>
  

