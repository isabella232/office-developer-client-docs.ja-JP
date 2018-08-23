---
title: SMTP ゲートウェイおよびトランスポートでの TNEF 関連付け
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 593f57d7-2891-40d1-a661-478a62d490ff
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: ec1d826ee2b3b46685a2c03dfaf45d2843869cc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804113"
---
# <a name="tnef-correlation-in-smtp-gateways-and-transports"></a><span data-ttu-id="27e8b-103">SMTP ゲートウェイおよびトランスポートでの TNEF 関連付け</span><span class="sxs-lookup"><span data-stu-id="27e8b-103">TNEF Correlation in SMTP Gateways and Transports</span></span>

  
  
<span data-ttu-id="27e8b-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="27e8b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="27e8b-105">ゲートウェイとインターネットに接続するためのトランスポートは、システムでは、SMTP を使用して、TNEF の相関関係を実装するために SMTP のメッセージ Id ヘッダーと、 **PR_TNEF_CORRELATION_KEY**プロパティの値を使用しているものに基づいています。</span><span class="sxs-lookup"><span data-stu-id="27e8b-105">Gateways and transports that connect to internet based systems, those that use SMTP, use the value of the MessageID SMTP header and the **PR_TNEF_CORRELATION_KEY** property to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="27e8b-106">送信メッセージのメッセージ Id ヘッダーの値は、 **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) のプロパティにコピーし、TNEF ストリームの[attMAPIProps](attmapiprops.md)属性内にエンコードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27e8b-106">The value of the MessageID header of the outbound message should be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property and encoded in the [attMAPIProps](attmapiprops.md) attribute of the TNEF stream.</span></span> <span data-ttu-id="27e8b-107">**PR_TNEF_CORRELATION_KEY**は、バイナリのプロパティにあるときにメッセージ Id 文字列。null 終端文字は、コピーでは比較に含まれているはずです。</span><span class="sxs-lookup"><span data-stu-id="27e8b-107">Note that **PR_TNEF_CORRELATION_KEY** is a binary property, while the MessageID is a string; the null terminator should be included in the copy and in the comparison.</span></span> 
  
<span data-ttu-id="27e8b-108">この手法は、MAPI ベースのメッセージング システムを Microsoft Exchange Server などのインターネットに接続するすべての Microsoft ソフトウェアによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="27e8b-108">This technique is used by all Microsoft software that connects MAPI-based messaging systems to the Internet, such as Microsoft Exchange Server.</span></span> <span data-ttu-id="27e8b-109">この方法は、任意の SMTP ゲートウェイとの相互運用性を最大化するために MAPI クライアントをサポートしているシステムに接続するためのトランスポートで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27e8b-109">This technique should be used by any SMTP gateways and transports that connect to systems that support MAPI clients in order to maximize interoperability.</span></span>
  

