---
title: 既定のメッセージ ストア
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: efa178eb-feb2-443f-8f6b-2ea53a456bf2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 3f7bf720f9105f6a81b832233cc648bc1d9ac91d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576912"
---
# <a name="default-message-stores"></a>既定のメッセージ ストア

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定のメッセージ ストアは、クライアント アプリケーションが汎用メッセージング タスクに使用できるものです。 既定のメッセージ ストアとしてメッセージ ストア プロバイダーを使用する場合に、メッセージ ストア プロバイダーにとって必要となるいくつかのオプション機能があります。 それらは次のとおりです。
  
- 受信トレイ、送信トレイ、および検索結果フォルダーなどの特別なフォルダーを実装します。
    
- 開封済みレポートと未読レポートを提供します。
    
- 受信メッセージと送信メッセージの送信を許可します。
    
- 任意のメッセージ クラスのメッセージの作成を許可します。
    
- 名前付きプロパティと複数値プロパティをサポートします。
    
- メッセージ ストア プロバイダーがトランスポート プロバイダーと密接に結合している場合でも、[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) メソッドをサポートします。 
    
- 関連するコンテンツ テーブルをサポートします。詳細については、[コンテンツ テーブル](contents-tables.md)を参照してください。
    
- 送信メッセージ キューにメッセージがある場合に、MAPI スプーラーの通知をサポートします。
    
## <a name="see-also"></a>関連項目



[MAPI メッセージ ストア プロバイダーの開発](developing-a-mapi-message-store-provider.md)

