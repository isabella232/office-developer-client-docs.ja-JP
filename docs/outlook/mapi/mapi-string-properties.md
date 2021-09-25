---
title: MAPI 文字列のプロパティ
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: '最終更新日: 2011 年 7 月 23 日'
ms.openlocfilehash: c6a8594e0849a500146842254feb95ee6ffc2c27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600800"
---
# <a name="mapi-string-properties"></a>MAPI 文字列のプロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
MAPI には、文字列プロパティを記述する 3 つの異なるプロパティの種類があります。
  
PT_TSTRING
  
PT_STRING8
  
PT_UNICODE
  
文字列プロパティは、最も一般的に、文字列プロパティとしてPT_TSTRING。 プロパティPT_TSTRINGは、UNICODE マクロが定義されたかどうかに応じて、他の文字列プロパティの種類の 1 つを条件付きでコンパイルします。 PT_STRING8 ANSI 形式の 8 ビットの null 終端文字文字列について説明します。PT_UNICODE、2 バイトの null 終端文字文字列について説明します。 
  
クライアントまたはサービス プロバイダー、またはクライアントとプロバイダーの両方で Unicode 文字文字列をサポートできます。 必須ではありません。 文字列のみをサポートするクライアントPT_STRING8 Unicode をサポートするプロバイダーを操作でき、その逆も同様です。 この相互運用性を有効にするには、クライアントとサービス プロバイダーは MAPI_UNICODE フラグを渡して、文字列の交換を伴うメソッドで Unicode がサポートされているかどうかを示します。 
  
たとえば、クライアントが Unicode をサポートし、フォルダーの表示名を取得する必要がある場合です。 クライアントのすべてのプロパティは、PT_TSTRINGを入力PT_UNICODE。 クライアントは、フォルダーの [IMAPIProp::GetProps](imapiprop-getprops.md)メソッドを呼び出して PR_DISPLAY_NAME ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) プロパティを取得すると **、MAPI_UNICODE** フラグを渡して、Unicode 形式で表示名文字列を返す要求を行います。 
  
クライアントとサービス プロバイダーは、メソッド呼び出しで文字セットを指定する場合は要求のみである点に注意する必要があります。 1 つまたは両方の文字セットをサポートする方法は、オブジェクトの実装者です。 ただし、サービス プロバイダーは、1 つのセットのみをサポートするプロバイダーよりも広範な配布を実現できるので、両方の文字セットをサポートしてください。 
  
文字列プロパティは、バイナリ プロパティ (プロパティの種類を使用するプロパティ) と同じサイズPT_BINARY。 大きなプロパティの操作を容易にするために、MAPI では、サービス プロバイダーがこれらのプロパティを設定してサイズ制限を適用できます。 これらの制限は、次に応じて異なります。
  
- プロパティが読み取りまたは書き込み中かどうか。
    
- サービス プロバイダーが **IMAPIProp メソッドを実装する** 方法。 
    
- メモリの制約など、ランタイムに関する考慮事項。
    
- 文字セットの変換に関する問題。 
    
サイズ制限は、大きなプロパティのすべての値を表示できない場合があるため、テーブルの列セットで使用する場合にも、文字列プロパティとバイナリ プロパティに配置できます。 多くのサービス プロバイダーは、テーブルで使用される大きな文字列プロパティまたはバイナリ プロパティを 255 バイトに切り詰めます。 
  
クライアントがオブジェクトの **GetProps** または **SetProps** メソッドを呼び出して、大きな文字列またはバイナリ プロパティを処理し、プロパティ サイズが原因で呼び出しが失敗すると、メソッドはエラー値 MAPI_E_NOT_ENOUGH_MEMORY を返します。 特定のプロパティに対して失敗している **GetProps** の場合、クライアントは [IMAPIProp::OpenProperty](imapiprop-openproperty.md) を呼び出し、IID_IStream をインターフェイス識別子として指定して **IStream** にアクセスを要求することで回復できます。 **OpenProperty を使用すると**、クライアントは、大きなプロパティの操作に適した **IStream** などのインターフェイスを使用して大きなプロパティを取得できます。 
  
## <a name="see-also"></a>関連項目



[MAPI のプロパティの概要](mapi-property-overview.md)

