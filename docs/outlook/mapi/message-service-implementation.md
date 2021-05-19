---
title: Message Service の実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: ef3820afbd4ae7ff04a3f54071e56f4e0a856109
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434033"
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

