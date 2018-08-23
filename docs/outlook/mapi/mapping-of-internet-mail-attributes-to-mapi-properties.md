---
title: インターネット メールの属性から MAPI のプロパティへのマッピング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 4d1bc5fc5a5e304d81ab4252a527d0e52b0d6e3c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19801544"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="63da3-103">インターネット メールの属性から MAPI のプロパティへのマッピング</span><span class="sxs-lookup"><span data-stu-id="63da3-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="63da3-104">**適用対象**: Outlook</span><span class="sxs-lookup"><span data-stu-id="63da3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="63da3-105">この付録では、MAPI トランスポート プロバイダーまたはインターネットに接続している MAPI 対応のゲートウェイを MAPI メッセージのプロパティと簡易メール転送プロトコル (SMTP) メッセージの属性の間で翻訳する必要がある方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="63da3-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="63da3-106">SMTP は、インターネットの多くで使用されているメッセージング プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="63da3-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="63da3-107">SMTP メッセージのヘッダーのセットを定義する-メッセージ エンベロープ、およびメッセージのコンテンツ形式。</span><span class="sxs-lookup"><span data-stu-id="63da3-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="63da3-108">SMTP は RFC 821 および RFC 822 は、公開されているいくつかの FTP と WWW のサイトで、インターネット上の 2 つのドキュメントのセットに完全に記載されています。</span><span class="sxs-lookup"><span data-stu-id="63da3-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="63da3-109">SMTP ベースのメール エージェントと通信するために使用する SMTP プロトコルについてを参照してください」簡易メール転送プロトコル、「RFC 821 で[http://www.rfc-editor.org](http://www.rfc-editor.org)です。</span><span class="sxs-lookup"><span data-stu-id="63da3-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="63da3-110">アドレス指定および標準のメッセージ ヘッダーで、RFC 822 の「標準の [形式の ARPA インターネット テキスト メッセージ、」を参照してください。 [http://www.rfc-editor.org](http://www.rfc-editor.org)。</span><span class="sxs-lookup"><span data-stu-id="63da3-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="63da3-111">MIME RFC 1521 を参照してください"MIME (多目的インターネット メール拡張機能) の一部 1: を指定して、インターネット メッセージの本文の形式を記述するための機構」で[http://www.rfc-editor.org](http://www.rfc-editor.org)です。</span><span class="sxs-lookup"><span data-stu-id="63da3-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [http://www.rfc-editor.org](http://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="63da3-112">MAPI プロパティ (およびその逆) の SMTP メッセージの属性のマッピングの目標は、さらに、ネイティブ SMTP メッセージの属性を使用してエンコードすることがあるが、MAPI メッセージの完全なコンテンツを確実に別の MAPI の間で交換できることを確認するにはコンポーネントをインターネット経由で通信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="63da3-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="63da3-113">このドキュメントは、マイクロソフトでは、このようなコンポーネントには既に作業に基づいています。</span><span class="sxs-lookup"><span data-stu-id="63da3-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="63da3-114">このドキュメントには、MAPI トランスポート、TNEF で SMTP と精通していることが前提としていますメールです。</span><span class="sxs-lookup"><span data-stu-id="63da3-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="63da3-115">豊富クリアするのではなく、簡潔にするよう努力しています。</span><span class="sxs-lookup"><span data-stu-id="63da3-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="63da3-116">通常、メールを MAPI に準拠した UA または MTA から、インターネットへの移動を参照して「送信」および MAPI コンポーネントへの移動、インターネットからメールを「受信」の意味です。</span><span class="sxs-lookup"><span data-stu-id="63da3-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

