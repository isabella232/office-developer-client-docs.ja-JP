---
title: Message Text/メッセージ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: fcbdec5adcb47ffac431a832cbb851ee4ebe16d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418548"
---
# <a name="message-text"></a><span data-ttu-id="d8b00-103">Message Text/メッセージ</span><span class="sxs-lookup"><span data-stu-id="d8b00-103">Message Text</span></span>

  
  
<span data-ttu-id="d8b00-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8b00-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8b00-105">MIME モードの送信メッセージの場合、コンテンツ タイプは添付ファイルの種類とメッセージ テキストの外観によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-105">For outbound messages in MIME mode, the content-type depends on whether there are attachments and what the message text looks like.</span></span> <span data-ttu-id="d8b00-106">添付ファイルがある場合、Content-type はマルチパート  _/_ ミックスです。メッセージ テキストと各添付ファイルは、それぞれ独自のコンテンツ タイプを持つメッセージ コンテンツの別個の部分になります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-106">If there are attachments, the Content-type is  _multipart/mixed;_ the message text and each attachment become a separate part of the message content, each with its own content-type.</span></span> <span data-ttu-id="d8b00-107">添付ファイルがない場合、メッセージのコンテンツ タイプは  _テキスト/_ プレーンで、パーツは 1 つのみです。</span><span class="sxs-lookup"><span data-stu-id="d8b00-107">If there are no attachments, the content-type of the message is  _text/plain_ and there is only one part.</span></span> 
  
<span data-ttu-id="d8b00-108">一部の行の長さが 140 文字を超えない限り、メッセージ テキストは行に折り返されません。</span><span class="sxs-lookup"><span data-stu-id="d8b00-108">The message text is not line-wrapped unless some line exceeds 140 characters in length.</span></span> <span data-ttu-id="d8b00-109">その場合、テキスト全体が 76 列にラップされ、引用符で囲まれた印刷可能なエンコードを使用して改行を保持します。</span><span class="sxs-lookup"><span data-stu-id="d8b00-109">If one does, the entire text is wrapped to 76 columns and the  _quoted-printable_ encoding is used to preserve line breaks.</span></span> <span data-ttu-id="d8b00-110">コンテンツ タイプは、次のようにメッセージ テキスト内に見つかった文字によって異なります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-110">The content-type depends on what characters are found in the message text, as follows:</span></span> 
  
- <span data-ttu-id="d8b00-111">7 ビット文字だけが見つかり、行の長さが 140 文字を超えない場合、メッセージは ASCII テキストになります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-111">If only 7-bit characters are found and no line exceeds 140 characters in length, the message is ASCII text.</span></span> <span data-ttu-id="d8b00-112">_コンテンツ タイプ: text/plain;charset=us-ascii_ (Content-Transfer-Encoding=7bit が想定されます)。</span><span class="sxs-lookup"><span data-stu-id="d8b00-112">_Content-type: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit is assumed.)</span></span> 
    
- <span data-ttu-id="d8b00-113">長い行または 8 ビット文字が見つかった場合、メッセージはテキストであり、文字セットはロケールによって決まります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-113">If long lines or 8-bit characters are found, the message is text and the character set is determined by the locale.</span></span> <span data-ttu-id="d8b00-114">ISO 標準 8859 で定義されている文字セットから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-114">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="d8b00-115">_コンテンツ タイプ: テキスト/プレーン、charset=iso-8859-1_ (または別の有効な文字セット)</span><span class="sxs-lookup"><span data-stu-id="d8b00-115">_Content-type: text/plain; charset=iso-8859-1_ (or another valid charset)</span></span> 
    
     <span data-ttu-id="d8b00-116">_Content-Transfer-Encoding: quoted-printable_</span><span class="sxs-lookup"><span data-stu-id="d8b00-116">_Content-Transfer-Encoding: quoted-printable_</span></span>
    
<span data-ttu-id="d8b00-117">受信 MIME メッセージの場合、最初のメッセージ コンテンツ パーツに _Content-type: \* text/_ (つまり、任意のテキストタイプ) が含められ、その文字セットが認識されると、その文字セットは PR_BODY ([PidTagBody)](pidtagbody-canonical-property.md)**に** マップされます。</span><span class="sxs-lookup"><span data-stu-id="d8b00-117">For inbound MIME messages, if the first message content part has  _Content-type: text/\*_ (that is, any text type) and its character set is recognized, it is mapped to **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span></span> <span data-ttu-id="d8b00-118">この条件を満たしていない最初のメッセージ コンテンツ パーツが添付ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-118">A first message content part not meeting this criterion becomes an attachment.</span></span> <span data-ttu-id="d8b00-119">後続のパーツも添付ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-119">Any subsequent parts also become attachments.</span></span>
  
<span data-ttu-id="d8b00-120">uuencode モードでは、MS Mail 3.x のように、送信メッセージのメッセージ テキストは 78 列に折り返されます。</span><span class="sxs-lookup"><span data-stu-id="d8b00-120">In uuencode mode, message text in outbound messages is line-wrapped to 78 columns, as for MS Mail 3.x.</span></span> <span data-ttu-id="d8b00-121">コンテンツ タイプは "text/plain" です。</span><span class="sxs-lookup"><span data-stu-id="d8b00-121">The content-type is "text/plain."</span></span> <span data-ttu-id="d8b00-122">このような状況下で元のメッセージの段落区切りを保持するには、ラップされたテキストで次の規則に従います。</span><span class="sxs-lookup"><span data-stu-id="d8b00-122">To preserve the original message's paragraph breaks under these circumstances, observe the following conventions in the wrapped text.</span></span> <span data-ttu-id="d8b00-123">1 行のテキストを終了する理由は 3 つあり、それぞれ独自の文字シーケンスがあります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-123">There are three possible reasons for ending a line of text, each with its own character sequence:</span></span>
  
- <span data-ttu-id="d8b00-124">行の折れ線。</span><span class="sxs-lookup"><span data-stu-id="d8b00-124">Line-break.</span></span> <span data-ttu-id="d8b00-125">元のテキストには、ユーザーが入力した改行 (段落記号) が含まれる。</span><span class="sxs-lookup"><span data-stu-id="d8b00-125">The original text contained a newline entered by the user (paragraph mark).</span></span> <span data-ttu-id="d8b00-126">トランスポートでは、前に空白がない改行にマップされます。</span><span class="sxs-lookup"><span data-stu-id="d8b00-126">In the transport, this maps to a newline with no preceding blanks.</span></span> <span data-ttu-id="d8b00-127">ユーザーが改行の前に空白を入力した場合は、空白を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-127">If the user enters a newline preceded by blanks, the blanks should be stripped out.</span></span>
    
- <span data-ttu-id="d8b00-128">Line-nobreak。</span><span class="sxs-lookup"><span data-stu-id="d8b00-128">Line-nobreak.</span></span> <span data-ttu-id="d8b00-129">元のテキストには、メッセージの 1 行に収まらない単語が長すぎます。</span><span class="sxs-lookup"><span data-stu-id="d8b00-129">The original text contained a word too long to fit on a single line of the message.</span></span> <span data-ttu-id="d8b00-130">トランスポートでは、改行の前に 2 つの空白がマップされます。</span><span class="sxs-lookup"><span data-stu-id="d8b00-130">In the transport, this maps to a newline preceded by two blanks.</span></span>
    
- <span data-ttu-id="d8b00-131">行折り返し。</span><span class="sxs-lookup"><span data-stu-id="d8b00-131">Line-wrap.</span></span> <span data-ttu-id="d8b00-132">元のテキストには改行が含めず、テキストが長すぎてメッセージの 1 行に収まらないが、2 つの単語の間で折れる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="d8b00-132">The original text contained no newline, the text is too long to fit on a single line of the message, but it can be broken between two words.</span></span> <span data-ttu-id="d8b00-133">トランスポートでは、改行の前に 1 つの空白が表示されます。</span><span class="sxs-lookup"><span data-stu-id="d8b00-133">In the transport, this maps to a newline preceded by a single blank.</span></span>
    

