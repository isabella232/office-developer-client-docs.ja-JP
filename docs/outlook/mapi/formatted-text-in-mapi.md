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
  
メッセージのテキストは、プレーン テキストまたは書式設定されたテキストを使用して保存および送信できます。 書式設定されたテキストは、1 つ以上のフォント、フォント サイズ、テキストの色など、外観を変更することでメッセージ テキストを強化します。 すべてのクライアントと可能な限り、すべてのメッセージ ストア プロバイダーが書式設定されたテキストをサポートする必要があります。 メッセージ内の書式設定されたテキストをサポートすると、メッセージの読みやすさが向上し、メッセージの処理が簡単かつ効率的になり、価値が向上します。
  
書式設定されたテキストは、さまざまな方法で実装できます。 最も一般的な方法は、リッチ テキスト形式 (RTF) です。 MAPI では、テキスト形式のテキスト情報を保持する **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md))、HTML の **場合** は PR_HTML ([PidTagHtml](pidtaghtml-canonical-property.md))、圧縮された RTF テキストの場合は PR_RTF_COMPRESSED ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) の **3** つの送信可能なプロパティを定義します。 書式設定されたバージョンのメッセージ テキストは、書式を設定せずにバージョンの 2 倍の大きいサイズにできます。そのため、RTF テキストはメッセージと一緒に転送され、PR_RTF_COMPRESSED プロパティに格納される前 **に圧縮** されます。 画面にメッセージを表示する時期は、MAPI によって提供されるユーティリティ関数を使用して圧縮解除されます。 
  
MAPI では、これらの 2 つのメッセージ テキスト プロパティとそれらの間の変換メカニズムを定義し、RTF 対応のクライアントが書式設定されたテキストをサポートしていないクライアントやメッセージング システムと相互運用できます。
  
### 

[テキストと書式設定の同期](synchronizing-text-and-formatting.md)
  
> RTF メッセージ テキストを書式設定と同期する方法について説明します。
    
[送信メッセージでの書式設定されたテキストのサポート: クライアントの責任](supporting-formatted-text-in-outgoing-messages-client-responsibilities.md)
  
> 送信メッセージで書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。
    
[受信メッセージの書式設定されたテキストのサポート: クライアントの責任](supporting-formatted-text-in-incoming-messages-client-responsibilities.md)
  
> 受信メッセージで書式設定されたテキストをサポートするためのクライアント アプリケーションの責任について説明します。
    
[書式設定されたテキストのサポート: メッセージ ストアの責任](supporting-formatted-text-message-store-responsibilities.md)
  
> 書式設定されたテキストをサポートするためのメッセージ ストアの責任について説明します。
    
[書式設定されたテキストのサポート: 添付ファイルのレンダリング](supporting-formatted-text-rendering-attachments.md)
  
> 添付ファイルをレンダリングする場所を選択する方法について説明します。
    
[書式設定されたテキストのサポート: ゲートウェイの責任](supporting-formatted-text-gateway-responsibilities.md)
  
> 送信および受信形式のテキスト メッセージのゲートウェイの責任について説明します。
    

