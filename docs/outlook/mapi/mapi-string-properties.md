---
title: MAPI 文字列のプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: '�ŏI�X�V��: 2011�N7��23��'
ms.openlocfilehash: 3e16a373ec35696f6d1a8ccc52263a1cf8570cfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572327"
---
# <a name="mapi-string-properties"></a>MAPI 文字列のプロパティ

  
  
**適用されます**: Outlook 2013 |Outlook 2016 
  
MAPI には、文字列のプロパティを記述する 3 つのプロパティの種類が用意されています。
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
文字列プロパティは、通常、PT_TSTRING として定義されます。 PT_TSTRING プロパティの型は他の文字列プロパティの型、UNICODE マクロが定義されているかどうかによって異なりますのいずれかに条件付きでコンパイルします。 PT_STRING8 8 ビット文字の null で終わる文字列を ANSI 形式での説明します。PT_UNICODE では、2 バイト文字の null で終わる文字列について説明します。 
  
Unicode 文字の文字列をサポートするか、クライアント、または、サービス プロバイダー、またはクライアントとプロバイダーの両方を選択できます。 必須ではありません。 PT_STRING8 文字列のみをサポートしているクライアントは、Unicode およびその逆の場合をサポートするプロバイダーを操作できます。 クライアントとサービス ・ プロバイダーは、この相互運用性を有効にするには、フラグ、文字の文字列の交換を伴う方法で Unicode がサポートされていることを示す MAPI_UNICODE フラグを渡します。 
  
たとえば、クライアントは、Unicode をサポートしているし、フォルダーの表示名を取得する必要があります。 すべてのクライアントの PT_TSTRING プロパティをコンパイルするには PT_UNICODE を入力します。 表示名の文字列が Unicode 形式で返されることを要求するのには MAPI_UNICODE フラグを渡す、クライアントがその**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) のプロパティを取得するためにフォルダーの[IMAPIProp::GetProps](imapiprop-getprops.md)のメソッドを呼び出すと、. 
  
クライアントとサービス ・ プロバイダーは、要求だけは、メソッドの呼び出しで文字セットを指定することに注意する必要があります。 オブジェクトの実装者は、1 つまたは両方の文字セットをサポートします。 ただし、サービス プロバイダーは、1 セットだけをサポートするプロバイダーよりも広範囲の配布を達成するためにできるため、両方の文字セットをサポートすることをお勧めします。 
  
文字列プロパティは、バイナリのプロパティと同様に非常に大きくなるまで拡張できます: プロパティを使用するプロパティは、PT_BINARY を入力します。 大きなプロパティの操作を容易にするためは、MAPI は、サイズの制限を適用するのには、これらのプロパティを設定するサービス プロバイダーを使用できます。 これらの制限は、によって異なります。
  
- プロパティがされているかどうかを読み取ったり書き込んだりします。
    
- サービス プロバイダーが、 **IMAPIProp**メソッドを実装する方法です。 
    
- メモリの制約などの実行時の考慮事項
    
- 文字セットの変換の問題です。 
    
文字列のサイズの制限を配置することもしもすべての大規模なプロパティの値が表示されるようにすることはないためテーブルの列で使用すると、バイナリのプロパティを設定します。 多くのサービス プロバイダーには、大きな文字列または 255 バイトをテーブルで使用されているバイナリのプロパティが切り捨てられます。 
  
クライアントは、大きな文字列またはバイナリのプロパティを操作するのには、オブジェクトの**GetProps**または**SetProps**メソッドを呼び出すし、プロパティのサイズであるため、呼び出しは失敗、エラー値 MAPI_E_NOT_ENOUGH_MEMORY を返します。 **GetProps**の特定のプロパティの不足している場合で[IMAPIProp::OpenProperty](imapiprop-openproperty.md)を呼び出すと、インターフェイス識別子として IID_IStream を指定することによってアクセスの**IStream**を要求するクライアントを回復できます。 クライアントは、 **OpenProperty**を使用するなど、大きなプロパティを操作するために適している**IStream**インターフェイスを使用して大規模なプロパティを取得できます。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

