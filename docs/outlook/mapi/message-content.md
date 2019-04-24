---
title: メッセージコンテンツ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357002"
---
# <a name="message-content"></a><span data-ttu-id="5652b-103">メッセージコンテンツ</span><span class="sxs-lookup"><span data-stu-id="5652b-103">Message Content</span></span>

  
  
<span data-ttu-id="5652b-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5652b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5652b-105">メッセージコンテンツには2つのエンコード方式があります。1つは MIME を使用し、もう1つは uuencode を使用します。</span><span class="sxs-lookup"><span data-stu-id="5652b-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="5652b-106">MIME は推奨されるエンコーディングです。</span><span class="sxs-lookup"><span data-stu-id="5652b-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="5652b-107">さらに、MAPI は、送信メッセージに TNEF 情報を含める必要があるかどうかを管理する、受信者ごとのプロパティである**PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) を定義します。</span><span class="sxs-lookup"><span data-stu-id="5652b-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="5652b-108">そのため、メッセージコンテンツをエンコードする方法は合計4つあります。</span><span class="sxs-lookup"><span data-stu-id="5652b-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="5652b-109">TNEF を使用した MIME</span><span class="sxs-lookup"><span data-stu-id="5652b-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="5652b-110">TNEF なしの MIME</span><span class="sxs-lookup"><span data-stu-id="5652b-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="5652b-111">TNEF を使用した uuencode</span><span class="sxs-lookup"><span data-stu-id="5652b-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="5652b-112">TNEF なしの uuencode</span><span class="sxs-lookup"><span data-stu-id="5652b-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="5652b-113">送信メッセージに対して MIME または uuencode を選択する方法が指定されていません。</span><span class="sxs-lookup"><span data-stu-id="5652b-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="5652b-114">次のプロパティは、TNEF から除外されます。 **\*PR_SENDER_**、 **PR_ATTACH_DATA_\***、 **PR_BODY**。</span><span class="sxs-lookup"><span data-stu-id="5652b-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="5652b-115">その他のすべての転送テーブルのメッセージプロパティは、TNEF ストリームに含まれています。</span><span class="sxs-lookup"><span data-stu-id="5652b-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="5652b-116">次の推奨事項は、実装がサポートする方法を決定できるパラメーターの一覧を提供することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="5652b-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="5652b-117">送信メッセージに MIME または uuencode を使用してエンコードするかどうか: boolean。</span><span class="sxs-lookup"><span data-stu-id="5652b-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="5652b-118">送信メッセージに使用する文字セット: string (charset パラメーターに直接コピーされる) または列挙 (内部的に文字セット文字列に変換されます)。</span><span class="sxs-lookup"><span data-stu-id="5652b-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

