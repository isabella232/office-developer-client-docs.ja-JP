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
ms.openlocfilehash: 1ad325c68241c8a3924909b4dbf42c9657e68352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338046"
---
# <a name="default-message-stores"></a>既定のメッセージ ストア

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
既定のメッセージ ストアは、クライアント アプリケーションが汎用メッセージング タスクに使用できるものです。既定のメッセージ ストアとしてメッセージ ストア プロバイダーを使用する場合に、メッセージ ストア プロバイダーにとって必要となるいくつかのオプション機能があります。これらは次のようになります。
  
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

