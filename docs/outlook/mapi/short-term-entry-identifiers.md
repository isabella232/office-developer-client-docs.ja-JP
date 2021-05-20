---
title: 短期エントリ ID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 1b361e025b631418eb63c5c74da264beadec2974
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439563"
---
# <a name="short-term-entry-identifiers"></a>短期エントリ ID

**適用対象**: Outlook 2013 | Outlook 2016 
  
短期間のエントリ識別子は、識別子を迅速に構築する必要があるときにサービス プロバイダーによってオブジェクトに割り当て、時間や距離の長持ちを必要としない場合に割り当てられます。 短期エントリ識別子の一意性は、現在のワークステーション上の現在のセッションの期間のみ保証されます。 通常、短期エントリ識別子は、それを表すオブジェクトが解放されるまで有効です。 
  
短期的なエントリ識別子は、テーブル内の行とダイアログ ボックス内のエントリに割り当てられます。ここで、参照用にデータをすばやく提供する必要があります。 たとえば、メッセージ ストア プロバイダーは、短期的なエントリ識別子をコンテンツ テーブル内のメッセージの行に、受信者テーブルの受信者に割り当てるとします。 

クライアントは、これらの短期エントリ識別子を使用して、テーブル行で表されるオブジェクトを開きます。 ただし **、OpenEntry** メソッドで使用できる長期エントリ識別子とは異なり、コンテナーの **OpenEntry** メソッドでは、短期エントリ識別子を使用する必要があります。 
  
## <a name="implementing-short-term-entry-identifiers"></a>短期エントリ識別子の実装

短期エントリ識別子を実装する最も一般的な方法は次のとおりです。
  
- 短期エントリ識別子を長期識別子と同じにし、すべてのフラグを設定解除します。 
    
- 短期エントリ識別子を長期識別子と異なって、すべてのフラグを設定します。 
    
クライアントは **、abFlags** メンバーを次のように調べることによって、2 番目の型の短期エントリ識別子を識別できます。 
  
```cpp
abFlags[0] = 0xFF;
 
```

一部のサービス プロバイダーは、1 つ以上のフラグをクリアして、より高い有効性を持つ短期エントリ識別子を作成します。 たとえば、次の **abFlags** メンバーは、複数日または複数のセッションで使用できる短期エントリ識別子を表します。 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

クライアントは、短期間のエントリ識別子をすばやく取得、使用、破棄します。 ほとんどの場合、長期エントリ識別子と同じ方法で使用できます。 テーブルから取得し **、OpenEntry** メソッドに渡し **、CompareEntryIDs** メソッドと比較できます。 1 つの例外は [、IMAPIProp::GetProps](imapiprop-getprops.md) メソッドから返されません。 **GetProps から返されるプロパティは**、常に長期的なエントリ識別子です。 
  
## <a name="see-also"></a>関連項目

- [MAPI エントリ識別子](mapi-entry-identifiers.md)

