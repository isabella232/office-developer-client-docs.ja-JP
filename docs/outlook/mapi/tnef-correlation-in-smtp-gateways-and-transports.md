---
title: SMTP ゲートウェイおよびトランスポートでの TNEF 相互関係
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 0a685e081d319c43daa583d95d163677e81f2480
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413669"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="374a2-103">SMTP ゲートウェイおよびトランスポートでの TNEF 相互関係</span><span class="sxs-lookup"><span data-stu-id="374a2-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="374a2-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="374a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="374a2-105">インターネットベースのシステムに接続するゲートウェイとトランスポート (SMTP を使用するもの) は、MessageID smtp ヘッダーの値と**PR_TNEF_CORRELATION_KEY**プロパティを使用して、TNEF の関連付けを実装します。</span><span class="sxs-lookup"><span data-stu-id="374a2-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="374a2-106">送信メッセージの MessageID ヘッダーの値は、 **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) プロパティにコピーし、TNEF ストリームの[attMAPIProps](attmapiprops.md)属性でエンコードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="374a2-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="374a2-107">**PR_TNEF_CORRELATION_KEY**はバイナリプロパティですが、MessageID が文字列である点に注意してください。null ターミネータはコピーと比較に含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="374a2-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="374a2-108">この手法は、microsoft Exchange Server などの MAPI ベースのメッセージングシステムをインターネットに接続するすべての microsoft ソフトウェアで使用されます。</span><span class="sxs-lookup"><span data-stu-id="374a2-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="374a2-109">この手法は、相互運用性を最大にするために、MAPI クライアントをサポートするシステムに接続するすべての SMTP ゲートウェイおよびトランスポートで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="374a2-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

