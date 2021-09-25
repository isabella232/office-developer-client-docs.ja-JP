---
title: Message Service の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 83fdf520f3e4b8acaa5d304f4c5a2b642ebcd71e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625218"
---
# <a name="message-service-implementation"></a>Message Service の実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージ サービスは、インストールと構成を簡略化するためにグループ化された 1 つ以上の関連サービス プロバイダーです。 すべてのサービス プロバイダーは、メッセージ サービスに含める必要があります。
  
1 つ以上のプロバイダーでメッセージ サービスを実装するには、次の手順を実行します。
  
1. メッセージ サービスを設計し、含めるサービス プロバイダーの数と種類を決定します。 メッセージ サービスを設計する方法の詳細については、「メッセージ サービスの設計 [」を参照してください](designing-a-message-service.md)。
    
2. メッセージ サービスにサービス プロバイダーをインストールするセットアップ プログラムを作成します。 メッセージ サービス セットアップ プログラムの作成の詳細については、「メッセージ サービスのインストールのサポート [」を参照してください](supporting-message-service-installation.md)。 
    
3. 構成を実行するエントリ ポイント関数を作成します。 メッセージ サービス エントリ ポイント関数の記述の詳細については、「Supporting [Message Service Configuration](supporting-message-service-configuration.md) and [MSGSERVICEENTRY」を参照してください](msgserviceentry.md)。 
    
4. メッセージ サービスがサポートするカスタム プロパティのプロパティ タグと有効な値の説明を含むパブリック ヘッダー ファイルを作成します。 
    
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

