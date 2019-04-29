---
title: アドレス帳の制限
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6ace8c03-45a7-484b-8c12-516ac0e40dc2
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 7419c174c1f68653794c2dbd836577e8dd3e596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432801"
---
# <a name="address-book-restrictions"></a>アドレス帳の制限

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
アドレス帳プロバイダーは、コンテナーのコンテンツテーブルに対して3種類の制限をサポートする必要があります。
  
- あいまいな名前のプロパティの制限
    
- インスタンスのキープロパティの制限
    
- プレフィックス付きの表示名コンテンツの制限
    
あいまいな名前の制限は、 **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)) プロパティを使用してアドレス帳コンテナー内のエントリで受信者名を一致させるプロパティの制限です。 **PR_ANR**プロパティの制限は、"最適な推測" の種類の検索として、アドレス帳プロバイダーが自分のコンテナーに最適な対応するプロパティを選択できるようにするものです。 たとえば、1つのアドレス帳プロバイダーは、受信者名を各コンテナーエントリの**PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) プロパティと一致させることによって**PR_ANR**制限を実装し、別のプロバイダーが PR_DISPLAY を使用する場合があります。 **_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
  
MAPI では、 **PR_ANR**制限の実装によって、十分なパフォーマンスとユーザーの満足度のバランスを取ることをお勧めします。 アドレス帳プロバイダーが、一致する件数が少なすぎる、または見つからないような制限を実装すると、ユーザーの満足度が低下する可能性があります。 アドレス帳プロバイダーの中には、識別可能な名前の制限に一致していても、ダイアログボックスには設定できない、識別可能な名前として知られているものをサポートしているものがあります。 
  
一般的な実装では、受信者の表示名を単語で解析して、すべての単語を含むエントリに一致させることができます。 nonconsecutive の単語が一致しているかどうか、単語の位置に対する感度などの詳細に注意してください。区切り文字の選択はさまざまです。 たとえば、解決される名前が "Bill L" の場合、一般的な**PR_ANR**制限は、次のエントリを一致として選択します。 
  
- Billy Larson
    
- Bill Lee
    
- Bill logan。 
    
- Sam Bill Lee
    
インスタンスキー制限または**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) プロパティの制限は、MAPI テーブルを表示するためにクライアントアプリケーションで使用されるリストボックスの実装で使用されます。 リストボックスの実装によっては、複数の選択を行ったり、上下にスクロールしたり、選択した最初の項目に戻ることができます。 この動作を実装するために、クライアントは[IMAPITable:: FindRow](imapitable-findrow.md)を呼び出し、 **PR_INSTANCE_KEY**プロパティのプロパティ制限をメソッドに渡します。 この制限をサポートするには、アドレス帳プロバイダーが必要です。 
  
表の表示に使用されるリストボックスのもう1つの機能は、一連の先頭文字に基づいてカーソルを配置する機能です。 ユーザーがプレフィックス文字の入力を開始すると、クライアントは、次の文字で始まる最初の項目にカーソルを移動します。 クライアントは、 **PR_DISPLAY_NAME**プロパティと FL_PREFIX あいまいレベルに基づくコンテンツ制限を使用してこの機能を実装します。 
  
## <a name="see-also"></a>関連項目



[MAPI テーブル](mapi-tables.md)

