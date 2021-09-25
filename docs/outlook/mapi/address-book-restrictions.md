---
title: アドレス帳の制限
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: decd8a746db45f60c96b008665d503eac5e3ec4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564429"
---
# <a name="address-book-restrictions"></a>アドレス帳の制限

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは、コンテナーのコンテンツ テーブルに対する 3 種類の制限をサポートする必要があります。
  
- あいまいな名前プロパティの制限
    
- インスタンス キープロパティの制限
    
- プレフィックス付き表示名のコンテンツ制限
    
あいまいな名前の制限は **、PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用して、受信者名とアドレス帳コンテナー内のエントリを一致するプロパティの制限です。 この **PR_ANR** プロパティの制限は、アドレス帳プロバイダーがコンテナーに最適な一致するプロパティを選択できる、"最適な推測" 型の検索です。 たとえば、あるアドレス帳プロバイダーは、受信者名を各コンテナー エントリの **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) プロパティと照合して PR_ANR 制限を実装します。一方、別のプロバイダーは **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)を使用する場合があります。
  
MAPI では、適切なパフォーマンスとユーザー **PR_ANRの** バランスを取る制限の実装をお勧めします。 アドレス帳プロバイダーが制限を実装して、一致する数が少なすぎたり、多すぎたりする場合、ユーザーの満足度が損なわれる可能性があります。 一部のアドレス帳プロバイダーは、ダイアログ ボックスでは表示できないが、あいまいな名前の制限に一致する識別名または一般的な名前と呼ばれる名前をサポートしています。 
  
一般的な実装は、受信者の表示名を単語に解析し、すべての単語を含むエントリと一致する場合があります。 単語の位置に対する感度、不起訴語が一致するかどうか、区切り文字の選択など、詳細に注意してください。 たとえば、解決する名前が "Bill L" の場合、一般的な制限PR_ANR一致として次のエントリが選択されます。 
  
- ビリー・ラーソン
    
- Bill Lee
    
- Bill Logan Jr. 
    
- Sam Bill Lee
    
MAPI テーブルを表示するためにクライアント アプリケーションで使用されるリスト ボックスの実装では、インスタンス キーの制限 **(PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの制限が使用されます。 一部のリスト ボックスの実装では、ユーザーは複数の選択を行い、上下にスクロールして、選択した最初の項目に戻る場合があります。 この動作を実装するために、クライアントは [IMAPITable::FindRow](imapitable-findrow.md)を呼び出し、PR_INSTANCE_KEY **プロパティの** プロパティ制限をメソッドに渡します。 この制限をサポートするには、アドレス帳プロバイダーが必要です。 
  
テーブル表示に使用されるリスト ボックスのもう 1 つの機能は、プレフィックス文字のセットに基づいてカーソルを配置する機能です。 ユーザーがプレフィックス文字の入力を開始すると、クライアントはカーソルをこれらの文字で始まる最初の項目に移動します。 クライアントは、PR_DISPLAY_NAME プロパティとファジー レベルに基 **FL_PREFIX** この機能を実装します。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

