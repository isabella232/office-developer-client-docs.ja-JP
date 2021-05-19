---
title: インターネット メール属性の MAPI プロパティへのマッピング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c0a71cbd3b6cdbef091e75ade5d190369a4626a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355819"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="55072-103">インターネット メール属性の MAPI プロパティへのマッピング</span><span class="sxs-lookup"><span data-stu-id="55072-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="55072-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55072-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55072-105">この付録では、インターネットに接続する MAPI トランスポート プロバイダーまたは MAPI 対応ゲートウェイが MAPI メッセージプロパティと簡易メール トランスポート プロトコル (SMTP) メッセージ属性の間でどのように変換されるのかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="55072-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="55072-106">SMTP は、インターネットの多くで使用されるメッセージング プロトコルです。</span><span class="sxs-lookup"><span data-stu-id="55072-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="55072-107">SMTP は、メッセージ ヘッダーのセット (メッセージ エンベロープ) とメッセージ コンテンツ形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="55072-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="55072-108">SMTP は、RFC 821 と RFC 822 という 2 つのドキュメントのセットで完全に文書化されています。これは、インターネット上の多数の FTP サイトと WWW サイトで確認できます。</span><span class="sxs-lookup"><span data-stu-id="55072-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="55072-109">SMTP ベースのメール エージェントとの通信に使用される SMTP プロトコルの詳細については、RFC 821「Simple Mail Transfer Protocol」を参照してください [https://www.rfc-editor.org](https://www.rfc-editor.org) 。</span><span class="sxs-lookup"><span data-stu-id="55072-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="55072-110">アドレス指定と標準メッセージ ヘッダーについては、RFC 822「STANDARD for the Format of ARPA Internet Text Messages」を参照してください [https://www.rfc-editor.org](https://www.rfc-editor.org) 。</span><span class="sxs-lookup"><span data-stu-id="55072-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="55072-111">MIME については、RFC 1521「MIME (多目的インターネット メール拡張機能) パート 1: インターネット メッセージの形式を指定および記述するためのメカニズム」を参照してください。 [https://www.rfc-editor.org](https://www.rfc-editor.org)</span><span class="sxs-lookup"><span data-stu-id="55072-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="55072-112">SMTP メッセージ属性を MAPI プロパティ (またはその逆) にマッピングする目的は、ネイティブの SMTP メッセージ属性を使用してエンコードできる以上の MAPI メッセージの完全なコンテンツを、インターネット上で通信する必要があるさまざまな MAPI コンポーネント間で確実に交換できるということです。</span><span class="sxs-lookup"><span data-stu-id="55072-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="55072-113">このドキュメントは、Microsoft でこのようなコンポーネントで既に行われた作業に基づいて作成されています。</span><span class="sxs-lookup"><span data-stu-id="55072-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="55072-114">このドキュメントでは、MAPI トランスポート、TNEF、および SMTP メールに精通している必要があります。</span><span class="sxs-lookup"><span data-stu-id="55072-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="55072-115">これは、明確ではなく簡潔になさる努力をしています。</span><span class="sxs-lookup"><span data-stu-id="55072-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="55072-116">「送信」とは、MAPI 準拠の UA または MTA からインターネットに移動するメールを指し、"受信" はインターネットから MAPI コンポーネントに移動するメールを指します。</span><span class="sxs-lookup"><span data-stu-id="55072-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

