---
title: MAPI 文字列のプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309521"
---
# <a name="mapi-string-properties"></a>MAPI 文字列のプロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI には、文字列プロパティを説明する3つの異なるプロパティの種類が用意されています。
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
文字列プロパティは、最も一般的に PT_TSTRING として定義されています。 PT_TSTRING プロパティの型は、UNICODE マクロが定義されているかどうかに応じて、他の文字列型のプロパティのうちの1つに条件付きでコンパイルされます。 PT_STRING8 は、ANSI 形式の8ビットの null 終端文字列を記述します。PT_UNICODE は、2バイトの null で終わる文字列を記述します。 
  
クライアントまたはサービスプロバイダー、あるいはクライアントとプロバイダーの両方が Unicode 文字列をサポートするかどうかを選択できます。 必須ではありません。 PT_STRING8 文字列のみをサポートするクライアントは、Unicode とその逆をサポートするプロバイダーで操作できます。 この相互運用性を有効にするために、クライアントとサービスプロバイダーはフラグ (MAPI_UNICODE フラグ) を渡して、文字列の交換を伴うメソッドで UNICODE がサポートされていることを示します。 
  
たとえば、クライアントが Unicode をサポートしており、フォルダーの表示名を取得する必要があるとします。 すべてのクライアントの PT_TSTRING プロパティは、PT_UNICODE 型にコンパイルされます。 クライアントがフォルダーの[imapiprop:: GetProps](imapiprop-getprops.md)メソッドを呼び出して、 **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを取得するときに、MAPI_UNICODE フラグを渡して、表示名文字列が UNICODE 形式で返されることを要求します。. 
  
クライアントおよびサービスプロバイダーは、メソッド呼び出しで文字セットを指定することは要求のみであることに注意する必要があります。 1つまたは両方の文字セットをサポートすることは、オブジェクトの実装側になります。 ただし、サービスプロバイダーは、1つのセットのみをサポートするプロバイダーよりも広範囲に分散を実現できるため、両方の文字セットをサポートすることをお勧めします。 
  
文字列プロパティは、バイナリプロパティと同じように大きくなる可能性があります。プロパティの型 PT_BINARY を使用するプロパティ。 大きなプロパティの操作を簡単にするために、MAPI では、これらのプロパティを設定してサイズ制限を適用することができます。 これらの制限は、以下によって異なる可能性があります。
  
- プロパティの読み取りまたは書き込みを行うかどうか。
    
- サービスプロバイダーが**imapiprop**メソッドを実装する方法。 
    
- メモリ制約などの実行時の考慮事項。
    
- 文字セットの変換の問題。 
    
サイズ制限は、大きなプロパティの値をすべて表示することができなくなる場合があるため、テーブルの列セットで使用されている場合は、文字列およびバイナリプロパティに配置することもできます。 多くのサービスプロバイダーは、表で使用されている大きな文字列またはバイナリのプロパティを255バイトに切り捨てます。 
  
クライアントがオブジェクトの**GetProps**または**setprops**メソッドを呼び出して、大きな文字列またはバイナリプロパティを処理するときに、プロパティのサイズが原因で呼び出しが失敗した場合、このメソッドはエラー値 MAPI_E_NOT_ENOUGH_MEMORY を返します。 特定のプロパティに対してエラーが発生している**GetProps**の場合、クライアントは[imapiprop:: openproperty](imapiprop-openproperty.md)を呼び出し、IID_IStream をインターフェイス識別子として指定して、アクセス用の**IStream**を要求することによって回復できます。 **openproperty**を使用すると、クライアントは、大きなプロパティの処理により適した**IStream**などのインターフェイスを使用して、ラージプロパティを取得できます。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

