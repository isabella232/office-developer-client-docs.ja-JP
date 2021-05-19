---
title: メッセージ配信レポートの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433081"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="98382-103">メッセージ配信レポートの送信</span><span class="sxs-lookup"><span data-stu-id="98382-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="98382-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="98382-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="98382-105">一部の基になるメッセージング システムは配信レポートをサポートし、一部はサポートしない場合があります。</span><span class="sxs-lookup"><span data-stu-id="98382-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="98382-106">トランスポート プロバイダーが、メッセージ配信レポートまたは配信以外のレポートをクライアント アプリケーションに送信できるかどうかを決定する方法は、個々のトランスポート プロバイダーに固有の実装の詳細です。</span><span class="sxs-lookup"><span data-stu-id="98382-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="98382-107">配信レポートをクライアント アプリケーションに送信できる場合、トランスポート プロバイダーは [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) メソッドを使用して、1 つ以上の受信者の配信が成功または失敗したと MAPI に通知します。</span><span class="sxs-lookup"><span data-stu-id="98382-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="98382-108">MAPI は、それらの受信者に対応する配信レポートまたは配信以外のレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="98382-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="98382-109">トランスポート プロバイダーは **、StatusRecips** を使用して、メッセージング システムにネイティブな受信配信レポートと配信不能レポートを MAPI 配信レポートと配信不能レポートに変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="98382-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

