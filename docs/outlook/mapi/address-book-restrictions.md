---
title: アドレス帳の制限
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 54cd90cac6c00e8cf274e0b78a1bfec32401bb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576513"
---
# <a name="address-book-restrictions"></a>アドレス帳の制限

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
アドレス帳プロバイダーがそのコンテナーのコンテンツ テーブルに 3 種類の制限をサポートするために必要です。
  
- あいまいな名前のプロパティの制限
    
- インスタンスのキー プロパティの制限
    
- プレフィックスが付けられた表示名のコンテンツの制限
    
あいまいな名前の制限とは、アドレス帳コンテナー内のエントリに受信者の名前を一致するように**PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用してプロパティの制限事項です。 **PR_ANR**プロパティの制限は、「最適な推測」アドレス帳プロバイダーがそのコンテナーに最も適した一致するプロパティを選択する、検索の型です。 たとえば、1 つのアドレス帳プロバイダーを実装**PR_ANR**制限各コンテナーのエントリの**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) プロパティと一致する受信者の名前で別のプロバイダーは、 **PR_DISPLAY を使用して可能性がありますが、名**([PidTagDisplayName](pidtagdisplayname-canonical-property.md))。
  
MAPI では、 **PR_ANR**の制限の実装が十分なパフォーマンスとユーザーの満足度の間でバランスを取ることをお勧めします。 アドレス帳プロバイダーなどの制限を実装する場合、ユーザーの満足度が侵害される可能性が少なすぎるか多すぎるの一致が見つかったことです。 いくつかのアドレス帳プロバイダー] ダイアログ ボックスで表示可能な項目はありませんが、あいまいな名前の制限に一致することができます識別、または共通名と呼ばれるものをサポートします。 
  
単語、単語のすべてを含む任意のエントリに一致する受信者の表示名を解析する一般的な実装があります。 位置の単語を小文字の区別などの詳細に注意、隣接していない複数の単語が一致するかどうか、および区切り文字の選択を変更できます。 などを解決するのには名前が「部品 L」の場合は、一般的な**PR_ANR**制限は次のエントリと一致する選択します。 
  
- Billy Larson
    
- Bill Lee
    
- 手形ローガン Jr。 
    
- Sam Bill Lee
    
インスタンス キーの制限、または、[プロパティ制限の**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) は、MAPI テーブルを表示するためにクライアント アプリケーションで使用されているリスト ボックスの実装で使用されます。 いくつかのリスト ボックスの実装には、ユーザーが複数選択するには、上にスクロールができるようにまたは、最初の項目に戻り値を選択します。 この動作を実装するには、クライアントは、 [IMAPITable::FindRow](imapitable-findrow.md)、 **PR_INSTANCE_KEY**プロパティにプロパティ制約をメソッドに渡すを呼び出します。 アドレス帳プロバイダーがこの制限をサポートするために必要です。 
  
テーブルの表示のためのリスト ボックスのほかの機能は、先頭の文字のセットに基づいたカーソルを配置することです。 ユーザーは、先頭の文字の入力を開始するとクライアントはこれらの文字で始まる最初の項目にカーソルを移動します。 クライアントは、 **PR_DISPLAY_NAME**プロパティと FL_PREFIX あいまいレベルに基づいて、コンテンツの制限でこの機能を実装します。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

