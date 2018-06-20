---
title: メッセージングのドメイン間で送信します。
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 65594253-66cd-486a-aa5b-0bc719f761f0
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 1fc5e4de63815c2cbfcb4818a9f6454af8c4d93b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803844"
---
# <a name="sending-across-messaging-domains"></a><span data-ttu-id="e14e6-103">メッセージングのドメイン間で送信します。</span><span class="sxs-lookup"><span data-stu-id="e14e6-103">Sending Across Messaging Domains</span></span>

  
  
<span data-ttu-id="e14e6-104">**適用されます**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e14e6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e14e6-105">メッセージング ドメインは、共通のアドレス形式を共有する 1 つまたは複数のメッセージング システムを表します。</span><span class="sxs-lookup"><span data-stu-id="e14e6-105">A messaging domain represents one or more messaging systems that share a common address format.</span></span> <span data-ttu-id="e14e6-106">複数のメッセージング ドメイン間の通信では、送信先のメッセージング ドメインの形式に元のメッセージング ドメインの形式で送信されたメッセージを変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e14e6-106">Communication across multiple messaging domains involves translating a message sent in the format of the original messaging domain into the format of the destination messaging domain.</span></span> <span data-ttu-id="e14e6-107">すべてのアドレスの形式に互換性があるために、元の形式から変換先の形式にアドレス情報を変換するゲートウェイが必要です。</span><span class="sxs-lookup"><span data-stu-id="e14e6-107">Because not all address formats are compatible, a gateway is needed to translate the addressing information from the source format into the destination format.</span></span> <span data-ttu-id="e14e6-108">検証するためにメッセージングのドメイン間で、クライアント アプリケーションは、MAPI プロパティの重要なアドレス情報を格納します。</span><span class="sxs-lookup"><span data-stu-id="e14e6-108">To ensure validity across messaging domains, client applications store important addressing information in MAPI properties.</span></span> <span data-ttu-id="e14e6-109">ゲートウェイが、プロパティの確認、変換を実行するさらに、翻訳し、送信先のメッセージング ドメインを使用できる形式に変更が必要な。</span><span class="sxs-lookup"><span data-stu-id="e14e6-109">In addition, gateways perform the translation, examining the properties known to need translation and changing them to a format that the destination messaging domain can use.</span></span>
  
<span data-ttu-id="e14e6-110">以前は、MAPI には、メッセージの現在の受信者リストを構成するユーザーのみに関連するアドレス指定情報が許可されます。</span><span class="sxs-lookup"><span data-stu-id="e14e6-110">Previously, MAPI allowed this addressing information to be associated with only the users who comprise a message's current recipient list.</span></span> <span data-ttu-id="e14e6-111">宛先リストの各メンバーを記述するプロパティでは、メッセージングのドメイン間での有効性を確保するのにはゲートウェイが必要な翻訳を生じた。</span><span class="sxs-lookup"><span data-stu-id="e14e6-111">The properties describing each member of the recipient list underwent the required translation by the gateway to ensure validity across messaging domains.</span></span> <span data-ttu-id="e14e6-112">ただし、アプリケーションをいくつかする、メッセージ アドレスなど、過去の受信者をされているユーザーに関する情報が含まれます、今後は、受信者をするか必要受信者になることはありませんが。</span><span class="sxs-lookup"><span data-stu-id="e14e6-112">However, some applications require that their messages include addressing information about users that perhaps were recipients in the past, will be recipients in the future, or will never be recipients.</span></span> <span data-ttu-id="e14e6-113">たとえば、ルーティング アプリケーションは、ユーザーのグループに指定した順序でメッセージを送信は、メッセージでこれらのユーザーのアドレス情報を埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="e14e6-113">For example, routing applications, which send messages in a specified order to a group of users, embed addressing information about these users in the messages.</span></span> <span data-ttu-id="e14e6-114">通常、埋め込まれた情報には、アドレスと将来の受信者では、おそらくこれもそれぞれの役割との回覧順序、パラメーター名、および受信者ごとに 1 つまたは複数のバイナリ識別子内の位置のアドレスの種類が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e14e6-114">The embedded information typically includes the address and address type of the future recipients, and perhaps also their roles and positions in the routing order, their names, and one or more binary identifiers per recipient.</span></span>
  
<span data-ttu-id="e14e6-115">MAPI にはこれらの nonrecipient のユーザーに関する情報を含むようにメッセージを有効にするには、nonrecipient この情報はメッセージングのドメイン間で正しく翻訳されてもいることを確認するための戦略が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e14e6-115">To enable messages to include information about these nonrecipient users, MAPI now includes a strategy for ensuring that this nonrecipient information is also translated correctly across messaging domains.</span></span> <span data-ttu-id="e14e6-116">この戦略は、ゲートウェイのマッピングが可能なプロパティの概念に基づいています。</span><span class="sxs-lookup"><span data-stu-id="e14e6-116">This strategy is based on the concept of gateway-mappable properties.</span></span>
  

