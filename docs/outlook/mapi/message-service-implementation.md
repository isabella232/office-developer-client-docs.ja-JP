---
title: メッセージ サービスの実装
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb529cc7-ad09-4f86-89bc-0e8ad29a3f38
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: c7007c01803676412b3efca8b7825b2ed8d863e6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582484"
---
# <a name="message-service-implementation"></a>メッセージ サービスの実装

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
メッセージ サービスは、インストールと構成を簡素化する目的でグループ化された 1 つまたは複数の関連のサービス ・ プロバイダーです。 すべてのサービス プロバイダーは、メッセージ サービスに含まれます。
  
メッセージ サービスを 1 つまたは複数のプロバイダーを実装するのには、次の手順を使用します。
  
1. 含まれるサービス プロバイダーの種類と個数を決定する、メッセージ サービスをデザインします。 メッセージ サービスを設計する方法の詳細については、[メッセージ サービスの設計](designing-a-message-service.md)を参照してください。
    
2. メッセージ サービスのサービス プロバイダーをインストールするセットアップ プログラムを作成します。 メッセージ サービスのセットアップ プログラムの作成の詳細については、[メッセージ サービスのインストールのサポート](supporting-message-service-installation.md)を参照してください。 
    
3. 構成を実行するエントリ ポイント関数を作成します。 メッセージ サービスのエントリの作成の詳細については関数をポイントし、[メッセージ サービスの構成のサポート](supporting-message-service-configuration.md)と[MSGSERVICEENTRY](msgserviceentry.md)を参照してください。 
    
4. プロパティ タグとメッセージ サービスをサポートする任意のカスタム プロパティの有効な値の説明を格納するパブリック ヘッダー ファイルを作成します。 
    
## <a name="see-also"></a>関連項目



[MAPI サービス プロバイダー](mapi-service-providers.md)

