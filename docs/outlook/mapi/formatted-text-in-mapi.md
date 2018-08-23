---
title: MAPI の書式付きテキスト
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d0ff834-253b-4e8c-a5be-6e4745a2a66c
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: bfaa4fd5f561c8138461db6ce8b9033c2a75b96b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580629"
---
# <a name="formatted-text-in-mapi"></a>MAPI の書式付きテキスト

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージのテキストは格納できるテキスト形式を使用して転送したり、書式設定されたテキスト。 書式設定されたテキストで、1 つまたは複数のフォント、フォント サイズなど、テキストの色の外観を変更することによりメッセージのテキストを強化します。 お勧めしますがすべてのクライアントとすべてのメッセージ ストア プロバイダーが書式設定されたテキストをサポート可能な限り、します。 メッセージの読みやすさを向上し、容易かつ効率的にメッセージの処理をすることによって値を追加するメッセージの書式設定されたテキストをサポートします。
  
書式設定されたテキストは、さまざまな方法で実装できます。 リッチ テキスト形式 (RTF) で、最も一般的な方法です。 MAPI メッセージのテキスト情報を保持するための 3 つの転送可能なプロパティを定義する: **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、 **PR_HTML** ([PidTagHtml](pidtaghtml-canonical-property.md))、HTML、 **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)のテキストに) 圧縮された rtf 形式のテキストにします。 メッセージ テキストの書式設定されたバージョンであるため 2 回バージョンと同じサイズ、書式を設定せず、rtf 形式のテキストは、メッセージの転送、 **PR_RTF_COMPRESSED**プロパティに格納する前に圧縮されています。 画面にメッセージを表示するのには時間がある場合は、MAPI によって提供されるユーティリティ関数を使用して圧縮されたことはできません。 
  
MAPI は、これら 2 つのメッセージ テキストのプロパティを定義し、それらの間の変換のためのメカニズム RTF に対応していないクライアントはクライアントとサポートしないメッセージング システムと相互運用できるように書式設定されたテキストです。
  
### 

[テキストと書式設定の同期](synchronizing-text-and-formatting.md)
  
> RTF メッセージ テキストの書式設定と同期を維持する方法について説明します。
    
[送信メッセージでの書式付きテキストのサポート: クライアントの責任](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> 送信するメッセージの書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。
    
[受信メッセージでの書式付きテキストのサポート: クライアントの責任](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> 受信メッセージの書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。
    
[書式付きテキストのサポート: メッセージ ストアの責任](supporting-formatted-text-message-store-responsibilities.md)
  
> 書式設定されたテキストをサポートするためのメッセージ ストアの役割について説明します。
    
[書式付きテキストのサポート: 添付ファイルの表示](supporting-formatted-text-rendering-attachments.md)
  
> 添付ファイルを表示する場所を選択する方法について説明します。
    
[書式付きテキストのサポート: ゲートウェイの責任](supporting-formatted-text-gateway-responsibilities.md)
  
> 書式設定されたテキスト メッセージを送信および受信のゲートウェイの役割について説明します。
    

