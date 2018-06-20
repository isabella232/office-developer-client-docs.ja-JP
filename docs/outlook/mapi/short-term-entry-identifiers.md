---
title: 短期的なエントリ id
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 948e007a-ad68-4abd-9720-204c6584beb5
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: f601971e61eb6430bef9d50b093642ee04b14044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803911"
---
# <a name="short-term-entry-identifiers"></a>短期的なエントリ id

**適用されます**: Outlook 
  
短期的なエントリの識別子は、識別子が迅速に構築する必要があり、最後の時間または距離にする必要はありません、オブジェクトへのサービス プロバイダーによって割り当てられます。 のみ期間中の現在のセッションでは、現在のワークステーションでは、短期的なエントリ id の一意性が保証されます。 通常、短期的なエントリ id は、それが表すオブジェクトが解放されるまでにのみ有効です。 
  
ダイアログ ボックスで、参照するために迅速にデータを提供する必要があるエントリをテーブル内の行には、短期的なエントリ id が割り当てられます。 などのコンテンツ テーブル内のメッセージの行に、受信者テーブル内の受信者に、メッセージ ストア プロバイダーは短期的なエントリの識別子を割り当てます。 

クライアントは、テーブルの行によって表されるオブジェクトを開く、これらの短期的なエントリ id を使用できます。 ただし、 **OpenEntry**メソッドのいずれかで使用できる長期のエントリ id とは異なり、短期的なエントリ id はコンテナーの**OpenEntry**メソッドで使用される必要があります。 
  
## <a name="implementing-short-term-entry-identifiers"></a>短期的なエントリ id を実装します。

短期的なエントリ id を実装する最も一般的な方法を以下に示します。
  
- すべてのフラグの設定を解除のまま、長期的な識別子として同じ短期のエントリ id を行っています。 
    
- 短期的なエントリの識別子のすべてのフラグの設定、長期的な識別子とは異なるを行っています。 
    
クライアントは、次のように、 **abFlags**メンバーを調べることでの 2 つ目の短期的なエントリ id を特定できます。 
  
```cpp
abFlags[0] = 0xFF;
 
```

サービス プロバイダーによってより妥当性のある短期のエントリの識別子を作成する 1 つまたは複数のフラグをクリアします。 などの次の**abFlags**メンバーは、複数の日または複数のセッションに使用できる短期的なエントリ id を表します。 
  
```cpp
abFlags[0] = 0xFF & ~MAPI_NOW;
abFlags[0] = 0xFF & ~MAPI_THISSESSION;
 
```

クライアントが簡単に取得、使用、および短期的なエントリ id を破棄します。 大部分は、長期のエントリ id と同じように使用することができます。 **OpenEntry**メソッドに渡され、 **CompareEntryIDs**メソッドと比較して、テーブルからは、それらを取得できます。 1 つの例外は、 [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドから返されますしないことです。 **GetProps**から返されるプロパティは、常に長期的なエントリの識別子です。 
  
## <a name="see-also"></a>関連項目

- [MAPI エントリの識別子](mapi-entry-identifiers.md)

