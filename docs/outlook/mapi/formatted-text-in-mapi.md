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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327469"
---
# <a name="formatted-text-in-mapi"></a><span data-ttu-id="1a647-103">MAPI の書式付きテキスト</span><span class="sxs-lookup"><span data-stu-id="1a647-103">Formatted Text in MAPI</span></span>

  
  
<span data-ttu-id="1a647-104">**適用対象**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a647-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a647-105">メッセージのテキストは、プレーンテキストまたは書式設定されたテキストを使用して保存および転送できます。</span><span class="sxs-lookup"><span data-stu-id="1a647-105">The text of a message can be stored and transmitted using plain text or formatted text.</span></span> <span data-ttu-id="1a647-106">書式設定されたテキストは、たとえば1つまたは複数のフォント、フォントサイズ、テキストの色などの外観を変更することによって、メッセージテキストを拡張します。</span><span class="sxs-lookup"><span data-stu-id="1a647-106">Formatted text enhances the message text by altering its appearance with, for example, one or more fonts, font sizes, or text colors.</span></span> <span data-ttu-id="1a647-107">すべてのクライアントと可能な限り、すべてのメッセージストアプロバイダーが書式設定されたテキストをサポートすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1a647-107">It is recommended that all clients and whenever possible, all message store providers, support formatted text.</span></span> <span data-ttu-id="1a647-108">メッセージで書式設定されたテキストをサポートすることで、メッセージの読みやすさが向上し、メッセージの処理がより簡単で効率的になるため、価値が高まります。</span><span class="sxs-lookup"><span data-stu-id="1a647-108">Supporting formatted text in messages adds value by improving message readability and making message handling easier and more efficient.</span></span>
  
<span data-ttu-id="1a647-109">書式設定されたテキストは、さまざまな方法で実装できます。</span><span class="sxs-lookup"><span data-stu-id="1a647-109">Formatted text can be implemented in a variety of ways.</span></span> <span data-ttu-id="1a647-110">リッチテキスト形式 (RTF) を使用する方法が最も一般的です。</span><span class="sxs-lookup"><span data-stu-id="1a647-110">The most common way is with the Rich Text Format (RTF).</span></span> <span data-ttu-id="1a647-111">MAPI は、メッセージテキスト情報を保持するための3つの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のプロパティを定義します。プレーンテキスト、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、および**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) )) を使用して、圧縮された RTF テキストを表示します。</span><span class="sxs-lookup"><span data-stu-id="1a647-111">MAPI defines three transmittable properties for holding message text information: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) for plain text, **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md)) for HTML, and **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) for RTF text that has been compressed.</span></span> <span data-ttu-id="1a647-112">書式設定されていない場合、メッセージテキストの書式設定されたバージョンは、2倍の大きさになる可能性があるので、RTF テキストはメッセージと共に転送されて**PR_RTF_COMPRESSED**プロパティに格納される前に圧縮されます。</span><span class="sxs-lookup"><span data-stu-id="1a647-112">Because the formatted version of a message text can be twice as large as the version without the formatting, the RTF text is compressed before it is transferred with the message and stored in the **PR_RTF_COMPRESSED** property.</span></span> <span data-ttu-id="1a647-113">メッセージを画面に表示する時間になると、MAPI で提供されるユーティリティ関数を使用して圧縮が解除されます。</span><span class="sxs-lookup"><span data-stu-id="1a647-113">When it is time to display the message on the screen, it is uncompressed using a utility function provided by MAPI.</span></span> 
  
<span data-ttu-id="1a647-114">MAPI は、RTF 対応クライアントが書式付きテキストをサポートしていないクライアントおよびメッセージングシステムと相互運用できるように、これら2つのメッセージテキストプロパティと、それらを変換するためのメカニズムを定義します。</span><span class="sxs-lookup"><span data-stu-id="1a647-114">MAPI defines these two message text properties and mechanisms for conversion between them so that RTF-aware clients can interoperate with clients and messaging systems that do not support formatted text.</span></span>
  
### 

[<span data-ttu-id="1a647-115">テキストと書式設定を同期する</span><span class="sxs-lookup"><span data-stu-id="1a647-115">Synchronizing Text and Formatting</span></span>](synchronizing-text-and-formatting.md)
  
> <span data-ttu-id="1a647-116">RTF メッセージテキストを書式設定と同期させる方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a647-116">Describes how to keep RTF message text synchronized with the formatting.</span></span>
    
[<span data-ttu-id="1a647-117">送信メッセージでの書式付きテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="1a647-117">Supporting Formatted Text in Outgoing Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> <span data-ttu-id="1a647-118">送信メッセージで書式設定されたテキストをサポートするためのクライアントアプリケーションの役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a647-118">Describes client application responsibilities for supporting formatted text in outgoing messages.</span></span>
    
[<span data-ttu-id="1a647-119">受信メッセージでの書式付きテキストのサポート: クライアントの責任</span><span class="sxs-lookup"><span data-stu-id="1a647-119">Supporting Formatted Text in Incoming Messages: Client Responsibilities</span></span>](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> <span data-ttu-id="1a647-120">受信メッセージで書式設定されたテキストをサポートするためのクライアントアプリケーションの役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a647-120">Describes client application responsibilities for supporting formatted text in incoming messages.</span></span>
    
[<span data-ttu-id="1a647-121">書式付きテキストのサポート: メッセージストアの責任</span><span class="sxs-lookup"><span data-stu-id="1a647-121">Supporting Formatted Text: Message Store Responsibilities</span></span>](supporting-formatted-text-message-store-responsibilities.md)
  
> <span data-ttu-id="1a647-122">書式設定されたテキストをサポートするメッセージストアの責任について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a647-122">Describes message store responsibilities for supporting formatted text.</span></span>
    
[<span data-ttu-id="1a647-123">書式付きテキストのサポート: 添付ファイルのレンダリング</span><span class="sxs-lookup"><span data-stu-id="1a647-123">Supporting Formatted Text: Rendering Attachments</span></span>](supporting-formatted-text-rendering-attachments.md)
  
> <span data-ttu-id="1a647-124">添付ファイルのレンダリング先を選択する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a647-124">Describes how to choose where attachments are rendered.</span></span>
    
[<span data-ttu-id="1a647-125">書式付きテキストのサポート: ゲートウェイの責任</span><span class="sxs-lookup"><span data-stu-id="1a647-125">Supporting Formatted Text: Gateway Responsibilities</span></span>](supporting-formatted-text-gateway-responsibilities.md)
  
> <span data-ttu-id="1a647-126">送信および受信の書式付きテキストメッセージのゲートウェイの役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="1a647-126">Describes the gateway responsibilities for outgoing and incoming formatted text messages.</span></span>
    

