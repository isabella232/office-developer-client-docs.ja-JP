---
title: メッセージサービスの実装
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
# <a name="message-service-implementation"></a>メッセージサービスの実装

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージサービスは、インストールと構成を簡素化するためにまとめられた1つ以上の関連するサービスプロバイダーです。 すべてのサービスプロバイダーがメッセージサービスに含まれている必要があります。
  
1つ以上のプロバイダーでメッセージサービスを実装するには、次の手順を使用します。
  
1. メッセージサービスを設計し、含めるサービスプロバイダーの数と種類を決定します。 メッセージサービスの設計方法の詳細については、「[メッセージサービスを設計](designing-a-message-service.md)する」を参照してください。
    
2. セットアッププログラムを作成して、メッセージサービスにサービスプロバイダーをインストールします。 メッセージサービスのセットアッププログラムの記述の詳細については、「[サポートメッセージサービスのインストール](supporting-message-service-installation.md)」を参照してください。 
    
3. 構成を実行するためのエントリポイント関数を作成します。 メッセージサービスのエントリポイント関数の記述の詳細については、「[サポートメッセージサービスの構成](supporting-message-service-configuration.md)」および「 [msgserviceentry](msgserviceentry.md)」を参照してください。 
    
4. メッセージサービスがサポートするカスタムプロパティについて、プロパティタグと有効な値の説明を含むパブリックヘッダーファイルを作成します。 
    
## <a name="see-also"></a>関連項目



[MAPI サービスプロバイダー](mapi-service-providers.md)

