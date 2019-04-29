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
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="6e4e5-103">メッセージ配信レポートの送信</span><span class="sxs-lookup"><span data-stu-id="6e4e5-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="6e4e5-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6e4e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6e4e5-105">いくつかの基礎となるメッセージングシステムは、配信レポートをサポートしています。</span><span class="sxs-lookup"><span data-stu-id="6e4e5-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="6e4e5-106">トランスポートプロバイダーが、メッセージ配信または配信不能レポートをクライアントアプリケーションに送信できるかどうかを判断する方法は、個々のトランスポートプロバイダーに固有の実装の詳細です。</span><span class="sxs-lookup"><span data-stu-id="6e4e5-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="6e4e5-107">配信レポートをクライアントアプリケーションに送信できる場合、トランスポートプロバイダーは[imapisupport:: StatusRecips](imapisupport-statusrecips.md)メソッドを使用して、1人以上の受信者に対して成功した、または失敗した配信を MAPI に通知します。</span><span class="sxs-lookup"><span data-stu-id="6e4e5-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="6e4e5-108">その後、MAPI は、これらの受信者に対応する配信レポートまたは配信不能レポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="6e4e5-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="6e4e5-109">また、トランスポートプロバイダーは、メッセージングシステムにネイティブである受信配信レポートと配信不能レポートを、 **StatusRecips**によって MAPI 配信および配信不能レポートに変換することもできます。</span><span class="sxs-lookup"><span data-stu-id="6e4e5-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

