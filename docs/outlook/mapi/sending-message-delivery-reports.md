---
title: メッセージ配信レポートの送信
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803868"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="750e7-103">メッセージ配信レポートの送信</span><span class="sxs-lookup"><span data-stu-id="750e7-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="750e7-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="750e7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="750e7-105">いくつかの基になるメッセージング システムが配信レポートをサポートし、ないものです。</span><span class="sxs-lookup"><span data-stu-id="750e7-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="750e7-106">トランスポート プロバイダーがクライアント アプリケーションにメッセージの配信または配信不能レポートを送信できるかどうかを決定する方法は、個々 のトランスポート プロバイダーに固有の実装の詳細です。</span><span class="sxs-lookup"><span data-stu-id="750e7-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="750e7-107">配信レポートは、クライアント アプリケーションに送信できる、トランスポート プロバイダーは 1 つまたは複数の受信者に対する配信の成功または失敗の MAPI を通知するために[IMAPISupport::StatusRecips](imapisupport-statusrecips.md)メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="750e7-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="750e7-108">MAPI では、配信または配信不能レポートが受信者に対応するが生成されます。</span><span class="sxs-lookup"><span data-stu-id="750e7-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="750e7-109">トランスポート プロバイダーは、 **StatusRecips**を使用して、MAPI 配信には、メッセージング システムにネイティブな受信の配信と配信不能レポートと配信不能レポートを変換できるも。</span><span class="sxs-lookup"><span data-stu-id="750e7-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

