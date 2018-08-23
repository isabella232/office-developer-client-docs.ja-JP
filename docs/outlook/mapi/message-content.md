---
title: メッセージの内容
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 85bd3f7db53f195295405fb0b02c25f084786a67
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586082"
---
# <a name="message-content"></a><span data-ttu-id="773e6-103">メッセージの内容</span><span class="sxs-lookup"><span data-stu-id="773e6-103">Message Content</span></span>

  
  
<span data-ttu-id="773e6-104">**適用されます**: Outlook 2013 |Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="773e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="773e6-105">メッセージの内容の 2 つの可能なエンコーディングがあります: 1 つ、他の MIME を使用して uuencode を使用しています。</span><span class="sxs-lookup"><span data-stu-id="773e6-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="773e6-106">MIME は、使用するエンコーディングします。</span><span class="sxs-lookup"><span data-stu-id="773e6-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="773e6-107">さらに、MAPI は、 **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) は、送信メッセージで TNEF 情報を含める必要があるかどうかを指定する、受信者ごとのプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="773e6-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="773e6-108">これは合計で 4 つの方法のメッセージ コンテンツのエンコードがあります。</span><span class="sxs-lookup"><span data-stu-id="773e6-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="773e6-109">TNEF で MIME します。</span><span class="sxs-lookup"><span data-stu-id="773e6-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="773e6-110">MIME TNEF なし</span><span class="sxs-lookup"><span data-stu-id="773e6-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="773e6-111">TNEF で uuencode</span><span class="sxs-lookup"><span data-stu-id="773e6-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="773e6-112">uuencode TNEF なし</span><span class="sxs-lookup"><span data-stu-id="773e6-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="773e6-113">MIME または uuencode 送信メッセージ用に選択する方法が指定されていません。</span><span class="sxs-lookup"><span data-stu-id="773e6-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="773e6-114">次のプロパティは TNEF から除外されます: **PR_SENDER_\***、 **PR_ATTACH_DATA_\***、 **PR_BODY**。</span><span class="sxs-lookup"><span data-stu-id="773e6-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="773e6-115">TNEF ストリームでは、他のすべてのメッセージを送信できるプロパティが含まれます。</span><span class="sxs-lookup"><span data-stu-id="773e6-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="773e6-116">実装がサポートする方法を決定するパラメーターの一覧を提供するは、次の方法が適しています。</span><span class="sxs-lookup"><span data-stu-id="773e6-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="773e6-117">送信メッセージの MIME または uuencode を使用してエンコードするかどうか: ブール値です。</span><span class="sxs-lookup"><span data-stu-id="773e6-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="773e6-118">送信メッセージに使用する一連の文字: (文字セット パラメーターに直接コピーされます) の文字列または (内部で変換する文字セットの文字列) を列挙します。</span><span class="sxs-lookup"><span data-stu-id="773e6-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

