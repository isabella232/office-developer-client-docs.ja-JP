---
title: インターネットメールの属性から MAPI プロパティへのマッピング
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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a><span data-ttu-id="a8c79-103">インターネットメールの属性から MAPI プロパティへのマッピング</span><span class="sxs-lookup"><span data-stu-id="a8c79-103">Mapping of Internet Mail Attributes to MAPI Properties</span></span>

  
  
<span data-ttu-id="a8c79-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8c79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8c79-105">この付録では、インターネットに接続する mapi トランスポートプロバイダーまたは mapi 対応ゲートウェイが mapi メッセージのプロパティと SMTP (Simple Mail transport Protocol) の各メッセージ属性との間で変換する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8c79-105">This appendix describes how a MAPI transport provider or MAPI-aware gateway which connects to the Internet should translate between MAPI message properties and Simple Mail Transport Protocol (SMTP) message attributes.</span></span> <span data-ttu-id="a8c79-106">SMTP は、インターネットの大部分で使用されるメッセージングプロトコルです。</span><span class="sxs-lookup"><span data-stu-id="a8c79-106">SMTP is the messaging protocol used on much of the Internet.</span></span> <span data-ttu-id="a8c79-107">SMTP は一連のメッセージヘッダー (メッセージエンベロープ) とメッセージコンテンツ形式を定義します。</span><span class="sxs-lookup"><span data-stu-id="a8c79-107">SMTP defines a set of message headers — the message envelope — and a message content format.</span></span> <span data-ttu-id="a8c79-108">SMTP は、rfc 821 と rfc 822 という2つのドキュメントのセットで完全にドキュメント化されています。これは、インターネット上のいくつかの FTP および WWW サイトにあります。</span><span class="sxs-lookup"><span data-stu-id="a8c79-108">SMTP is fully documented in a set of two documents, RFC 821 and RFC 822, which can be found at a number of FTP and WWW sites on the Internet.</span></span>
  
<span data-ttu-id="a8c79-109">smtp ベースのメールエージェントとの通信に使用される smtp プロトコルの詳細については、RFC 821 「Simple mail Transfer protocol [https://www.rfc-editor.org](https://www.rfc-editor.org),」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8c79-109">For information on the SMTP protocol used to communicate with SMTP-based mail agents, see RFC 821, "Simple Mail Transfer Protocol," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="a8c79-110">アドレス指定と標準的なメッセージヘッダーについては、「RFC 822,」を参照してください[https://www.rfc-editor.org](https://www.rfc-editor.org)。インターネットテキストメッセージの形式については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8c79-110">For addressing and standard message headers, see RFC 822, "Standard for the Format of ARPA Internet Text Messages," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="a8c79-111">mime の場合は、「RFC 1521, "mime (多目的インターネットメール拡張機能) パート 1: インターネットメッセージ本文の形式を指定して記述する[https://www.rfc-editor.org](https://www.rfc-editor.org)ための機構」 () を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a8c79-111">For MIME, see RFC 1521, "MIME (Multipurpose Internet Mail Extensions) Part One: Mechanisms for Specifying and Describing the Format of Internet Message Bodies," at [https://www.rfc-editor.org](https://www.rfc-editor.org).</span></span>
  
<span data-ttu-id="a8c79-112">smtp メッセージ属性を mapi プロパティにマッピングする目的 (およびその逆) は、ネイティブの smtp メッセージ属性を使用してエンコードできる mapi メッセージの完全なコンテンツを、さまざまな mapi 間で確実に交換できるようにすることです。インターネット経由で通信する必要があるコンポーネント。</span><span class="sxs-lookup"><span data-stu-id="a8c79-112">The goal of mapping SMTP message attributes to MAPI properties (and vice versa) is to ensure that the full content of MAPI messages, over and above that which can be encoded using native SMTP message attributes, can be reliably exchanged among different MAPI components that must communicate over the Internet.</span></span> <span data-ttu-id="a8c79-113">このドキュメントは、Microsoft のこのようなコンポーネントで既に実行された作業に基づいています。</span><span class="sxs-lookup"><span data-stu-id="a8c79-113">This document is based on work already done on such components at Microsoft.</span></span> 
  
<span data-ttu-id="a8c79-114">このドキュメントでは、MAPI トランスポート、TNEF、および SMTP メールに精通していることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="a8c79-114">This document assumes familiarity with MAPI transports, TNEF, and SMTP mail.</span></span> <span data-ttu-id="a8c79-115">abundantly clear ではなく簡潔なものにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8c79-115">It strives to be concise rather than abundantly clear.</span></span>
  
<span data-ttu-id="a8c79-116">慣例として、"送信" とは、mapi 準拠の UA または MTA からインターネットへのメールを指し、"受信" とはインターネットから mapi コンポーネントへのメールを送信することを指します。</span><span class="sxs-lookup"><span data-stu-id="a8c79-116">As a convention, "outbound" refers to mail traveling from a MAPI-compliant UA or MTA to the Internet, and "inbound" refers to mail traveling from the Internet to a MAPI component.</span></span>
  

