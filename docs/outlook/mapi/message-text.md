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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356869"
---
# <a name="message-text"></a><span data-ttu-id="bb1b0-103">Message Text/メッセージ</span><span class="sxs-lookup"><span data-stu-id="bb1b0-103">Message Text</span></span>

  
  
<span data-ttu-id="bb1b0-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb1b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb1b0-105">MIME モードの送信メッセージの場合、コンテンツタイプは、添付ファイルがあるかどうかと、メッセージテキストがどのようなものかによって異なります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-105">For outbound messages in MIME mode, the content-type depends on whether there are attachments and what the message text looks like.</span></span> <span data-ttu-id="bb1b0-106">添付ファイルがある場合、コンテンツタイプは_マルチパート/mixed です。_ メッセージテキストと各添付ファイルは、それぞれ独自のコンテンツタイプを持つメッセージコンテンツの独立した部分になります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-106">If there are attachments, the Content-type is  _multipart/mixed;_ the message text and each attachment become a separate part of the message content, each with its own content-type.</span></span> <span data-ttu-id="bb1b0-107">添付ファイルが存在しない場合、メッセージのコンテンツタイプは_テキスト/プレーン_で、パーツは1つしかありません。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-107">If there are no attachments, the content-type of the message is  _text/plain_ and there is only one part.</span></span> 
  
<span data-ttu-id="bb1b0-108">メッセージテキストは、一部の行が140文字を超えていない限り、行の折り返しを行いません。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-108">The message text is not line-wrapped unless some line exceeds 140 characters in length.</span></span> <span data-ttu-id="bb1b0-109">1つの場合は、テキスト全体が76列に折り返され、_引用符で囲まれた印刷可能_なエンコードを使用して改行を保持します。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-109">If one does, the entire text is wrapped to 76 columns and the  _quoted-printable_ encoding is used to preserve line breaks.</span></span> <span data-ttu-id="bb1b0-110">コンテンツタイプは、次のように、メッセージテキストに含まれる文字によって決まります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-110">The content-type depends on what characters are found in the message text, as follows:</span></span> 
  
- <span data-ttu-id="bb1b0-111">7ビット文字のみが検索され、長さが140文字を超える行がない場合、メッセージは ASCII テキストになります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-111">If only 7-bit characters are found and no line exceeds 140 characters in length, the message is ASCII text.</span></span> <span data-ttu-id="bb1b0-112">_コンテンツタイプ: text/plain、charset = us-ascii_(コンテンツ転送-エンコード = 7bit が想定されます。)</span><span class="sxs-lookup"><span data-stu-id="bb1b0-112">_Content-type: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit is assumed.)</span></span> 
    
- <span data-ttu-id="bb1b0-113">長い行または8ビットの文字が検出された場合、メッセージはテキストで、文字セットはロケールによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-113">If long lines or 8-bit characters are found, the message is text and the character set is determined by the locale.</span></span> <span data-ttu-id="bb1b0-114">ISO 規格8859で定義されている文字セットから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-114">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="bb1b0-115">_コンテンツタイプ: text/plain、charset = iso-8859-1_(または別の有効な文字セット)</span><span class="sxs-lookup"><span data-stu-id="bb1b0-115">_Content-type: text/plain; charset=iso-8859-1_ (or another valid charset)</span></span> 
    
     <span data-ttu-id="bb1b0-116">_Content-Transfer-Encoding: quoted-printable_</span><span class="sxs-lookup"><span data-stu-id="bb1b0-116">_Content-Transfer-Encoding: quoted-printable_</span></span>
    
<span data-ttu-id="bb1b0-117">受信 MIME メッセージの場合、最初のメッセージコンテンツパーツの_コンテンツタイプが text/\* _ (つまり、任意のテキストタイプ)、文字セットが認識される場合は、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) にマップされます。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-117">For inbound MIME messages, if the first message content part has  _Content-type: text/\*_ (that is, any text type) and its character set is recognized, it is mapped to **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span></span> <span data-ttu-id="bb1b0-118">この条件を満たさない最初のメッセージコンテンツパーツは、添付ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-118">A first message content part not meeting this criterion becomes an attachment.</span></span> <span data-ttu-id="bb1b0-119">その後のパーツも添付ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-119">Any subsequent parts also become attachments.</span></span>
  
<span data-ttu-id="bb1b0-120">uuencode モードでは、送信メッセージのメッセージテキストは、78列に改行されます (MS Mail 3 .x の場合)。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-120">In uuencode mode, message text in outbound messages is line-wrapped to 78 columns, as for MS Mail 3.x.</span></span> <span data-ttu-id="bb1b0-121">コンテンツタイプは "text/plain" です。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-121">The content-type is "text/plain."</span></span> <span data-ttu-id="bb1b0-122">このような状況で元のメッセージの段落区切りを保持するには、折り返したテキストで次の規則に従います。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-122">To preserve the original message's paragraph breaks under these circumstances, observe the following conventions in the wrapped text.</span></span> <span data-ttu-id="bb1b0-123">テキストの行を終了する理由は3つあり、それぞれに独自の文字シーケンスがあります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-123">There are three possible reasons for ending a line of text, each with its own character sequence:</span></span>
  
- <span data-ttu-id="bb1b0-124">改行します。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-124">Line-break.</span></span> <span data-ttu-id="bb1b0-125">元のテキストには、ユーザーが入力した改行 (段落記号) が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-125">The original text contained a newline entered by the user (paragraph mark).</span></span> <span data-ttu-id="bb1b0-126">トランスポートでは、これは、先行ブランクがない改行にマップされます。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-126">In the transport, this maps to a newline with no preceding blanks.</span></span> <span data-ttu-id="bb1b0-127">ユーザーが空白で始まる改行を入力した場合は、空白を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-127">If the user enters a newline preceded by blanks, the blanks should be stripped out.</span></span>
    
- <span data-ttu-id="bb1b0-128">線-nobreak</span><span class="sxs-lookup"><span data-stu-id="bb1b0-128">Line-nobreak.</span></span> <span data-ttu-id="bb1b0-129">元のテキストに長い単語が含まれているため、メッセージの1行に収めることができません。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-129">The original text contained a word too long to fit on a single line of the message.</span></span> <span data-ttu-id="bb1b0-130">トランスポートでは、これは2つの空白で始まる改行にマップされます。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-130">In the transport, this maps to a newline preceded by two blanks.</span></span>
    
- <span data-ttu-id="bb1b0-131">行の折り返し</span><span class="sxs-lookup"><span data-stu-id="bb1b0-131">Line-wrap.</span></span> <span data-ttu-id="bb1b0-132">元のテキストに改行が含まれていません。テキストが長すぎてメッセージの1行に収めることはできませんが、2つの単語の間で区切ることができます。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-132">The original text contained no newline, the text is too long to fit on a single line of the message, but it can be broken between two words.</span></span> <span data-ttu-id="bb1b0-133">トランスポートでは、これは1つの空白で始まる改行にマップされます。</span><span class="sxs-lookup"><span data-stu-id="bb1b0-133">In the transport, this maps to a newline preceded by a single blank.</span></span>
    

