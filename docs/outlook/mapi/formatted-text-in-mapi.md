---
title: MAPI の書式付きテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7f37d65e4beb328c2c92cf0c2ab28586af6bee45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408090"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="21500-103">MAPI の書式付きテキスト</span><span class="sxs-lookup"><span data-stu-id="21500-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="21500-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21500-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21500-105">メッセージのテキストは、プレーン テキストまたは書式設定されたテキストを使用して保存および送信できます。</span><span class="sxs-lookup"><span data-stu-id="21500-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="21500-106">書式設定されたテキストは、1 つ以上のフォント、フォント サイズ、テキストの色など、外観を変更することでメッセージ テキストを強化します。</span><span class="sxs-lookup"><span data-stu-id="21500-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="21500-107">すべてのクライアントと可能な限り、すべてのメッセージ ストア プロバイダーが書式設定されたテキストをサポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="21500-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="21500-108">メッセージ内の書式設定されたテキストをサポートすると、メッセージの読みやすさが向上し、メッセージの処理が簡単かつ効率的になり、価値が向上します。</span><span class="sxs-lookup"><span data-stu-id="21500-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="21500-109">書式設定されたテキストは、さまざまな方法で実装できます。</span><span class="sxs-lookup"><span data-stu-id="21500-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="21500-110">最も一般的な方法は、リッチ テキスト形式 (RTF) です。</span><span class="sxs-lookup"><span data-stu-id="21500-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="21500-111">MAPI では、テキスト形式のテキスト情報を保持する **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、HTML の **場合** は PR_HTML ([PidTagHtml](pidtaghtml-canonical-property.md))、圧縮された RTF テキストの場合は PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) の **3** つの送信可能なプロパティを定義します。</span><span class="sxs-lookup"><span data-stu-id="21500-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="21500-112">書式設定されたバージョンのメッセージ テキストは、書式を設定せずにバージョンの 2 倍の大きいサイズにできます。そのため、RTF テキストはメッセージと一緒に転送され、PR_RTF_COMPRESSED プロパティに格納される前 **に圧縮** されます。</span><span class="sxs-lookup"><span data-stu-id="21500-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="21500-113">画面にメッセージを表示する時期は、MAPI によって提供されるユーティリティ関数を使用して圧縮解除されます。</span><span class="sxs-lookup"><span data-stu-id="21500-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="21500-114">MAPI では、これらの 2 つのメッセージ テキスト プロパティとそれらの間の変換メカニズムを定義し、RTF 対応のクライアントが書式設定されたテキストをサポートしていないクライアントやメッセージング システムと相互運用できます。</span><span class="sxs-lookup"><span data-stu-id="21500-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="21500-115">テキストと書式設定の同期</span><span class="sxs-lookup"><span data-stu-id="21500-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="21500-116">RTF メッセージ テキストを書式設定と同期する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="21500-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="21500-117">送信メッセージでの書式設定されたテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="21500-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="21500-118">送信メッセージで書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="21500-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="21500-119">受信メッセージの書式設定されたテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="21500-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="21500-120">受信メッセージで書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="21500-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="21500-121">書式設定されたテキストのサポート: メッセージ ストアの責任</span><span class="sxs-lookup"><span data-stu-id="21500-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="21500-122">書式設定されたテキストをサポートするためのメッセージ ストアの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="21500-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="21500-123">書式設定されたテキストのサポート: 添付ファイルのレンダリング</span><span class="sxs-lookup"><span data-stu-id="21500-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="21500-124">添付ファイルをレンダリングする場所を選択する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="21500-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="21500-125">書式設定されたテキストのサポート: ゲートウェイの責任</span><span class="sxs-lookup"><span data-stu-id="21500-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="21500-126">送信および受信形式のテキスト メッセージのゲートウェイの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="21500-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

