---
title: メッセージ コンテンツ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435461"
---
# <a name="message-content"></a><span data-ttu-id="6966f-103">メッセージ コンテンツ</span><span class="sxs-lookup"><span data-stu-id="6966f-103">Message Content</span></span>

  
  
<span data-ttu-id="6966f-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6966f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6966f-105">メッセージ コンテンツには、MIME を使用するエンコードと uuencode を使用するエンコードの 2 つがあります。</span><span class="sxs-lookup"><span data-stu-id="6966f-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="6966f-106">MIME が優先エンコードです。</span><span class="sxs-lookup"><span data-stu-id="6966f-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="6966f-107">さらに、MAPI は **、TNEF** 情報を送信メッセージに含めるかどうかを制御する受信者ごとのプロパティ PR_SEND_RICH_INFO ([PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)を定義します。</span><span class="sxs-lookup"><span data-stu-id="6966f-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="6966f-108">したがって、メッセージ コンテンツをエンコードする方法は合計 4 種類あります。</span><span class="sxs-lookup"><span data-stu-id="6966f-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="6966f-109">TNEF を含む MIME</span><span class="sxs-lookup"><span data-stu-id="6966f-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="6966f-110">TNEF なしの MIME</span><span class="sxs-lookup"><span data-stu-id="6966f-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="6966f-111">TNEF を含む uuencode</span><span class="sxs-lookup"><span data-stu-id="6966f-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="6966f-112">TNEF のない uuencode</span><span class="sxs-lookup"><span data-stu-id="6966f-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="6966f-113">送信メッセージに MIME または uuencode を選択する方法は指定されていません。</span><span class="sxs-lookup"><span data-stu-id="6966f-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="6966f-114">次のプロパティは、TNEF から除外されます **\* 。PR_SENDER_、PR_ATTACH_DATA_、PR_BODY。** **\*** </span><span class="sxs-lookup"><span data-stu-id="6966f-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="6966f-115">他のすべての送信可能なメッセージ プロパティは、TNEF ストリームに含まれます。</span><span class="sxs-lookup"><span data-stu-id="6966f-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="6966f-116">次の提案は、実装がサポートする方法を決定できるパラメーターの一覧を提供することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="6966f-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="6966f-117">送信メッセージに MIME または uuencode を使用してエンコードするかどうかを指定します。ブール型 (boolean) です。</span><span class="sxs-lookup"><span data-stu-id="6966f-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="6966f-118">送信メッセージに使用する文字セット: string (charset パラメーターに直接コピー) または列挙 (内部で文字セット文字列に変換)。</span><span class="sxs-lookup"><span data-stu-id="6966f-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

