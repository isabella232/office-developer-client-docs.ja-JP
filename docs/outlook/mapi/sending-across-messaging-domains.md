---
title: メッセージングドメイン間での送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ddbaa4aeacf17f2c266ccc0ff963d005f9e403ec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339719"
---
# <a name="sending-across-messaging-domains"></a><span data-ttu-id="64855-103">メッセージングドメイン間での送信</span><span class="sxs-lookup"><span data-stu-id="64855-103">Sending Across Messaging Domains</span></span>

  
  
<span data-ttu-id="64855-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64855-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64855-105">メッセージングドメインは、共通のアドレス形式を共有する1つ以上のメッセージングシステムを表します。</span><span class="sxs-lookup"><span data-stu-id="64855-105">A messaging domain represents one or more messaging systems that share a common address format.</span></span> <span data-ttu-id="64855-106">複数のメッセージングドメイン間の通信には、元のメッセージングドメインの形式で送信されたメッセージを宛先のメッセージングドメインの形式に変換することが含まれます。</span><span class="sxs-lookup"><span data-stu-id="64855-106">Communication across multiple messaging domains involves translating a message sent in the format of the original messaging domain into the format of the destination messaging domain.</span></span> <span data-ttu-id="64855-107">すべてのアドレス形式に互換性がないため、アドレス指定情報をソース形式から送信先の形式に変換するためにゲートウェイが必要になります。</span><span class="sxs-lookup"><span data-stu-id="64855-107">Because not all address formats are compatible, a gateway is needed to translate the addressing information from the source format into the destination format.</span></span> <span data-ttu-id="64855-108">メッセージングドメイン間での有効性を確保するため、クライアントアプリケーションは重要なアドレス指定情報を MAPI プロパティに格納します。</span><span class="sxs-lookup"><span data-stu-id="64855-108">To ensure validity across messaging domains, client applications store important addressing information in MAPI properties.</span></span> <span data-ttu-id="64855-109">さらに、ゲートウェイは変換を実行し、変換が必要であることがわかっているプロパティを調べて、送信先のメッセージングドメインで使用できる形式に変更します。</span><span class="sxs-lookup"><span data-stu-id="64855-109">In addition, gateways perform the translation, examining the properties known to need translation and changing them to a format that the destination messaging domain can use.</span></span>
  
<span data-ttu-id="64855-110">以前は、MAPI でこのアドレス指定情報に関連付けられるのは、メッセージの現在の受信者リストを構成しているユーザーのみに制限されていました。</span><span class="sxs-lookup"><span data-stu-id="64855-110">Previously, MAPI allowed this addressing information to be associated with only the users who comprise a message's current recipient list.</span></span> <span data-ttu-id="64855-111">受信者一覧の各メンバーを説明するプロパティは、メッセージングドメイン間での有効性を確保するために、ゲートウェイによって必要な変換を underwent ます。</span><span class="sxs-lookup"><span data-stu-id="64855-111">The properties describing each member of the recipient list underwent the required translation by the gateway to ensure validity across messaging domains.</span></span> <span data-ttu-id="64855-112">ただし、一部のアプリケーションでは、以前に受信者としている可能性があるユーザーに関するアドレス情報、今後受信者になる、受信者にならないものが要求されることがあります。</span><span class="sxs-lookup"><span data-stu-id="64855-112">However, some applications require that their messages include addressing information about users that perhaps were recipients in the past, will be recipients in the future, or will never be recipients.</span></span> <span data-ttu-id="64855-113">たとえば、指定された順序でメッセージをユーザーのグループに送信するルーティングアプリケーションでは、これらのユーザーに関するアドレス指定情報をメッセージに埋め込むことができます。</span><span class="sxs-lookup"><span data-stu-id="64855-113">For example, routing applications, which send messages in a specified order to a group of users, embed addressing information about these users in the messages.</span></span> <span data-ttu-id="64855-114">通常、埋め込まれた情報には、将来の受信者のアドレスとアドレスの種類、さらには、ルーティング順序の役割と位置、名前、および1つまたは複数のバイナリ識別子 (受信者ごと) も含まれています。</span><span class="sxs-lookup"><span data-stu-id="64855-114">The embedded information typically includes the address and address type of the future recipients, and perhaps also their roles and positions in the routing order, their names, and one or more binary identifiers per recipient.</span></span>
  
<span data-ttu-id="64855-115">このような受信者以外のユーザーに関する情報をメッセージに含めることができるようにするために、MAPI には、このような受信者ではない情報がメッセージングドメイン間で正しく変換されるようにするための方法が含まれています。</span><span class="sxs-lookup"><span data-stu-id="64855-115">To enable messages to include information about these nonrecipient users, MAPI now includes a strategy for ensuring that this nonrecipient information is also translated correctly across messaging domains.</span></span> <span data-ttu-id="64855-116">この戦略は、ゲートウェイマッピングされたプロパティの概念に基づいています。</span><span class="sxs-lookup"><span data-stu-id="64855-116">This strategy is based on the concept of gateway-mappable properties.</span></span>
  

