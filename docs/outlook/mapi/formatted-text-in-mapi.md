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
# <a name="formatted-text-in-mapi"></a>MAPI の書式付きテキスト

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージのテキストは、プレーンテキストまたは書式設定されたテキストを使用して保存および転送できます。 書式設定されたテキストは、たとえば1つまたは複数のフォント、フォントサイズ、テキストの色などの外観を変更することによって、メッセージテキストを拡張します。 すべてのクライアントと可能な限り、すべてのメッセージストアプロバイダーが書式設定されたテキストをサポートすることをお勧めします。 メッセージで書式設定されたテキストをサポートすることで、メッセージの読みやすさが向上し、メッセージの処理がより簡単で効率的になるため、価値が高まります。
  
書式設定されたテキストは、さまざまな方法で実装できます。 リッチテキスト形式 (RTF) を使用する方法が最も一般的です。 MAPI は、メッセージテキスト情報を保持するための3つの**PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) のプロパティを定義します。プレーンテキスト、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、および**PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md) )) を使用して、圧縮された RTF テキストを表示します。 書式設定されていない場合、メッセージテキストの書式設定されたバージョンは、2倍の大きさになる可能性があるので、RTF テキストはメッセージと共に転送されて**PR_RTF_COMPRESSED**プロパティに格納される前に圧縮されます。 メッセージを画面に表示する時間になると、MAPI で提供されるユーティリティ関数を使用して圧縮が解除されます。 
  
MAPI は、RTF 対応クライアントが書式付きテキストをサポートしていないクライアントおよびメッセージングシステムと相互運用できるように、これら2つのメッセージテキストプロパティと、それらを変換するためのメカニズムを定義します。
  
### 

[テキストと書式設定を同期する](synchronizing-text-and-formatting.md)
  
> RTF メッセージテキストを書式設定と同期させる方法について説明します。
    
[送信メッセージでの書式付きテキストのサポート: クライアントの責任](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> 送信メッセージで書式設定されたテキストをサポートするためのクライアントアプリケーションの役割について説明します。
    
[受信メッセージでの書式付きテキストのサポート: クライアントの責任](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> 受信メッセージで書式設定されたテキストをサポートするためのクライアントアプリケーションの役割について説明します。
    
[書式付きテキストのサポート: メッセージストアの責任](supporting-formatted-text-message-store-responsibilities.md)
  
> 書式設定されたテキストをサポートするメッセージストアの責任について説明します。
    
[書式付きテキストのサポート: 添付ファイルのレンダリング](supporting-formatted-text-rendering-attachments.md)
  
> 添付ファイルのレンダリング先を選択する方法について説明します。
    
[書式付きテキストのサポート: ゲートウェイの責任](supporting-formatted-text-gateway-responsibilities.md)
  
> 送信および受信の書式付きテキストメッセージのゲートウェイの役割について説明します。
    

