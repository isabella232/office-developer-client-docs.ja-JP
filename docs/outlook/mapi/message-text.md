---
title: メッセージ テキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 9dba148646678f0740c5b2c338ae345ecd76dfac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19801639"
---
# <a name="message-text"></a><span data-ttu-id="fb0c2-103">メッセージ テキスト</span><span class="sxs-lookup"><span data-stu-id="fb0c2-103">Message Text</span></span>

  
  
<span data-ttu-id="fb0c2-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fb0c2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fb0c2-105">MIME モードでの送信メッセージのコンテンツの種類によって異なるかどうかは添付ファイルとメッセージのテキストは次のようにあります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-105">For outbound messages in MIME mode, the content-type depends on whether there are attachments and what the message text looks like.</span></span> <span data-ttu-id="fb0c2-106">添付ファイルがある場合は、コンテンツ タイプは、メッセージ テキスト_マルチパートと混合して_各添付ファイルがメッセージの内容、それぞれに独自のコンテンツの種類の別の部分になります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-106">If there are attachments, the Content-type is  _multipart/mixed;_ the message text and each attachment become a separate part of the message content, each with its own content-type.</span></span> <span data-ttu-id="fb0c2-107">添付ファイルがない場合、メッセージのコンテンツ タイプ_と_1 つだけの部分があります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-107">If there are no attachments, the content-type of the message is  _text/plain_ and there is only one part.</span></span> 
  
<span data-ttu-id="fb0c2-108">メッセージのテキストがない行が折り返されていくつかの行は、140 文字の長さを超えない限り、します。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-108">The message text is not line-wrapped unless some line exceeds 140 characters in length.</span></span> <span data-ttu-id="fb0c2-109">76 列にテキスト全体をラップが存在する場合、および_引用符で囲まれた印刷可能な_エンコーディングを使用して、改行を保持します。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-109">If one does, the entire text is wrapped to 76 columns and the  _quoted-printable_ encoding is used to preserve line breaks.</span></span> <span data-ttu-id="fb0c2-110">コンテンツ タイプは、どのような文字は、メッセージ テキストを次のようにによって異なります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-110">The content-type depends on what characters are found in the message text, as follows:</span></span> 
  
- <span data-ttu-id="fb0c2-111">7 ビットの文字が見つかるし、行を超えると 140 文字の長さでない、だけの場合、メッセージは、ASCII テキストになります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-111">If only 7-bit characters are found and no line exceeds 140 characters in length, the message is ASCII text.</span></span> <span data-ttu-id="fb0c2-112">_コンテンツの種類: テキスト/形式; charset =、us-ascii_(コンテンツ転送エンコード = 7 ビットであると見なされます)。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-112">_Content-type: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit is assumed.)</span></span> 
    
- <span data-ttu-id="fb0c2-113">長い行、または 8 ビットの文字が見つかった場合、メッセージ テキストは、文字セットは、ロケールによって決まります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-113">If long lines or 8-bit characters are found, the message is text and the character set is determined by the locale.</span></span> <span data-ttu-id="fb0c2-114">ISO 8859 の標準で定義されている文字セットから選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-114">It should be chosen from the character sets defined by ISO standard 8859.</span></span> <span data-ttu-id="fb0c2-115">_コンテンツの種類: テキスト/形式; charset = iso 8859-1_(または別の有効な文字セット)</span><span class="sxs-lookup"><span data-stu-id="fb0c2-115">_Content-type: text/plain; charset=iso-8859-1_ (or another valid charset)</span></span> 
    
     <span data-ttu-id="fb0c2-116">_Content-Transfer-Encoding: quoted-printable_</span><span class="sxs-lookup"><span data-stu-id="fb0c2-116">_Content-Transfer-Encoding: quoted-printable_</span></span>
    
<span data-ttu-id="fb0c2-117">受信 MIME メッセージの場合は、最初のメッセージ コンテンツの一部が_コンテンツの種類: テキスト/\* _ (つまり、すべてのテキスト型) とは、その文字セットを認識、 **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) にマップされています。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-117">For inbound MIME messages, if the first message content part has  _Content-type: text/\*_ (that is, any text type) and its character set is recognized, it is mapped to **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)).</span></span> <span data-ttu-id="fb0c2-118">この条件を満たしていない最初のメッセージ コンテンツ部分では、添付ファイルになります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-118">A first message content part not meeting this criterion becomes an attachment.</span></span> <span data-ttu-id="fb0c2-119">任意の残りの部分は、添付ファイルにもなります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-119">Any subsequent parts also become attachments.</span></span>
  
<span data-ttu-id="fb0c2-120">Uuencode モードでは、送信メッセージのメッセージ テキストは、MS Mail の場合と、78 の列に行が折り返されて 3.x。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-120">In uuencode mode, message text in outbound messages is line-wrapped to 78 columns, as for MS Mail 3.x.</span></span> <span data-ttu-id="fb0c2-121">コンテンツ タイプは、「テキスト/形式」です。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-121">The content-type is "text/plain."</span></span> <span data-ttu-id="fb0c2-122">このような状況下で元のメッセージの段落の区切りを保持するには、ラップされたテキストでは、次の規則を確認します。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-122">To preserve the original message's paragraph breaks under these circumstances, observe the following conventions in the wrapped text.</span></span> <span data-ttu-id="fb0c2-123">それぞれ独自の文字シーケンスを持つテキストの行を終了する 3 つの原因があります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-123">There are three possible reasons for ending a line of text, each with its own character sequence:</span></span>
  
- <span data-ttu-id="fb0c2-124">改行します。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-124">Line-break.</span></span> <span data-ttu-id="fb0c2-125">元のテキストには、(段落記号) のユーザーによって入力された改行文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-125">The original text contained a newline entered by the user (paragraph mark).</span></span> <span data-ttu-id="fb0c2-126">トランスポートの前の空白なしに改行文字にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-126">In the transport, this maps to a newline with no preceding blanks.</span></span> <span data-ttu-id="fb0c2-127">場合は空白に続く改行文字を入力すると、空白を削除した必要があります。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-127">If the user enters a newline preceded by blanks, the blanks should be stripped out.</span></span>
    
- <span data-ttu-id="fb0c2-128">Nobreak の行です。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-128">Line-nobreak.</span></span> <span data-ttu-id="fb0c2-129">元のテキストには、メッセージの 1 行に収まらない単語が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-129">The original text contained a word too long to fit on a single line of the message.</span></span> <span data-ttu-id="fb0c2-130">トランスポートの前に 2 つの空白で改行文字にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-130">In the transport, this maps to a newline preceded by two blanks.</span></span>
    
- <span data-ttu-id="fb0c2-131">行の折り返しです。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-131">Line-wrap.</span></span> <span data-ttu-id="fb0c2-132">元のテキストに改行文字が含まれていません、メッセージの 1 行に収まるようにテキストが長すぎますが、2 つの単語の間で分割できます。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-132">The original text contained no newline, the text is too long to fit on a single line of the message, but it can be broken between two words.</span></span> <span data-ttu-id="fb0c2-133">トランスポートの 1 つの空白に続く改行文字にマッピングします。</span><span class="sxs-lookup"><span data-stu-id="fb0c2-133">In the transport, this maps to a newline preceded by a single blank.</span></span>
    

