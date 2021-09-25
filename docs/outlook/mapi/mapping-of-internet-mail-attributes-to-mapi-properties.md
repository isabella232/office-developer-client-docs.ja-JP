---
title: インターネット メール属性の MAPI プロパティへのマッピング
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 79d1d2ba-34fe-4851-918f-adbc69c20eee
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c9f77ea7ba56e7c559cf9b4c41a2d6f4d742b866
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604734"
---
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>インターネット メール属性の MAPI プロパティへのマッピング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この付録では、インターネットに接続する MAPI トランスポート プロバイダーまたは MAPI 対応ゲートウェイが MAPI メッセージプロパティと簡易メール トランスポート プロトコル (SMTP) メッセージ属性の間でどのように変換されるのかについて説明します。 SMTP は、インターネットの多くで使用されるメッセージング プロトコルです。 SMTP は、メッセージ ヘッダーのセット (メッセージ エンベロープ) とメッセージ コンテンツ形式を定義します。 SMTP は、RFC 821 と RFC 822 という 2 つのドキュメントのセットで完全に文書化されています。これは、インターネット上の多数の FTP サイトと WWW サイトで確認できます。
  
SMTP ベースのメール エージェントとの通信に使用される SMTP プロトコルの詳細については、RFC 821「Simple Mail Transfer Protocol」を参照してください [https://www.rfc-editor.org](https://www.rfc-editor.org) 。
  
アドレス指定と標準メッセージ ヘッダーについては、RFC 822「STANDARD for the Format of ARPA Internet Text Messages」を参照してください [https://www.rfc-editor.org](https://www.rfc-editor.org) 。
  
MIME については、RFC 1521「MIME (多目的インターネット メール拡張機能) パート 1: インターネット メッセージの形式を指定および記述するためのメカニズム」を参照してください。 [https://www.rfc-editor.org](https://www.rfc-editor.org)
  
SMTP メッセージ属性を MAPI プロパティ (またはその逆) にマッピングする目的は、ネイティブの SMTP メッセージ属性を使用してエンコードできる以上の MAPI メッセージの完全なコンテンツを、インターネット上で通信する必要があるさまざまな MAPI コンポーネント間で確実に交換できるということです。 このドキュメントは、Microsoft でこのようなコンポーネントで既に行われた作業に基づいて作成されています。 
  
このドキュメントでは、MAPI トランスポート、TNEF、および SMTP メールに精通している必要があります。 これは、明確ではなく簡潔になさる努力をしています。
  
「送信」とは、MAPI 準拠の UA または MTA からインターネットに移動するメールを指し、"受信" はインターネットから MAPI コンポーネントに移動するメールを指します。
  

