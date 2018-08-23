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
ms.openlocfilehash: 54443001e3cb14603c8f8f798f2a4068d73b00eb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568064"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>インターネット メールの属性から MAPI のプロパティへのマッピング

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
この付録では、MAPI トランスポート プロバイダーまたはインターネットに接続している MAPI 対応のゲートウェイを MAPI メッセージのプロパティと簡易メール転送プロトコル (SMTP) メッセージの属性の間で翻訳する必要がある方法について説明します。 SMTP は、インターネットの多くで使用されているメッセージング プロトコルです。 SMTP メッセージのヘッダーのセットを定義する-メッセージ エンベロープ、およびメッセージのコンテンツ形式。 SMTP は RFC 821 および RFC 822 は、公開されているいくつかの FTP と WWW のサイトで、インターネット上の 2 つのドキュメントのセットに完全に記載されています。
  
SMTP ベースのメール エージェントと通信するために使用する SMTP プロトコルについてを参照してください」簡易メール転送プロトコル、「RFC 821 で[http://www.rfc-editor.org](http://www.rfc-editor.org)です。
  
アドレス指定および標準のメッセージ ヘッダーで、RFC 822 の「標準の [形式の ARPA インターネット テキスト メッセージ、」を参照してください。 [http://www.rfc-editor.org](http://www.rfc-editor.org)。
  
MIME RFC 1521 を参照してください"MIME (多目的インターネット メール拡張機能) の一部 1: を指定して、インターネット メッセージの本文の形式を記述するための機構」で[http://www.rfc-editor.org](http://www.rfc-editor.org)です。
  
MAPI プロパティ (およびその逆) の SMTP メッセージの属性のマッピングの目標は、さらに、ネイティブ SMTP メッセージの属性を使用してエンコードすることがあるが、MAPI メッセージの完全なコンテンツを確実に別の MAPI の間で交換できることを確認するにはコンポーネントをインターネット経由で通信する必要があります。 このドキュメントは、マイクロソフトでは、このようなコンポーネントには既に作業に基づいています。 
  
このドキュメントには、MAPI トランスポート、TNEF で SMTP と精通していることが前提としていますメールです。 豊富クリアするのではなく、簡潔にするよう努力しています。
  
通常、メールを MAPI に準拠した UA または MTA から、インターネットへの移動を参照して「送信」および MAPI コンポーネントへの移動、インターネットからメールを「受信」の意味です。
  

