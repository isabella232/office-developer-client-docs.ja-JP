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
# <a name="mapping-of-internet-mail-attributes-to-mapi-properties"></a>インターネットメールの属性から MAPI プロパティへのマッピング

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
この付録では、インターネットに接続する mapi トランスポートプロバイダーまたは mapi 対応ゲートウェイが mapi メッセージのプロパティと SMTP (Simple Mail transport Protocol) の各メッセージ属性との間で変換する方法について説明します。 SMTP は、インターネットの大部分で使用されるメッセージングプロトコルです。 SMTP は一連のメッセージヘッダー (メッセージエンベロープ) とメッセージコンテンツ形式を定義します。 SMTP は、rfc 821 と rfc 822 という2つのドキュメントのセットで完全にドキュメント化されています。これは、インターネット上のいくつかの FTP および WWW サイトにあります。
  
smtp ベースのメールエージェントとの通信に使用される smtp プロトコルの詳細については、RFC 821 「Simple mail Transfer protocol [https://www.rfc-editor.org](https://www.rfc-editor.org),」を参照してください。
  
アドレス指定と標準的なメッセージヘッダーについては、「RFC 822,」を参照してください[https://www.rfc-editor.org](https://www.rfc-editor.org)。インターネットテキストメッセージの形式については、「」を参照してください。
  
mime の場合は、「RFC 1521, "mime (多目的インターネットメール拡張機能) パート 1: インターネットメッセージ本文の形式を指定して記述する[https://www.rfc-editor.org](https://www.rfc-editor.org)ための機構」 () を参照してください。
  
smtp メッセージ属性を mapi プロパティにマッピングする目的 (およびその逆) は、ネイティブの smtp メッセージ属性を使用してエンコードできる mapi メッセージの完全なコンテンツを、さまざまな mapi 間で確実に交換できるようにすることです。インターネット経由で通信する必要があるコンポーネント。 このドキュメントは、Microsoft のこのようなコンポーネントで既に実行された作業に基づいています。 
  
このドキュメントでは、MAPI トランスポート、TNEF、および SMTP メールに精通していることを前提としています。 abundantly clear ではなく簡潔なものにする必要があります。
  
慣例として、"送信" とは、mapi 準拠の UA または MTA からインターネットへのメールを指し、"受信" とはインターネットから mapi コンポーネントへのメールを送信することを指します。
  

