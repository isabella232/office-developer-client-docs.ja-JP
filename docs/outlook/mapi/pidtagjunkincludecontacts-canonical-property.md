---
title: PidTagJunkIncludeContacts 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: df31fbcfd5f238c99e4b5a82771cea1bccf0403f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59595232"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>PidTagJunkIncludeContacts 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
連絡先フォルダー内の連絡先の電子メール アドレスがスパム フィルターに関して特別に処理されるかどうかを示します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|識別子:  <br/> |0x6100  <br/> |
|データの種類 :   <br/> |PT_LONG  <br/> |
|エリア:  <br/> |スパム  <br/> |
   
## <a name="remarks"></a>注釈

"0x00000001" に設定されている場合、これらの電子メール アドレスは、これらのアドレスからのメールが "迷惑メールではない" として扱われるなど、迷惑メール ルール制限の "信頼済み" 連絡先メール アドレス部分を設定する必要があります。 "0x00000000" に設定されている場合、連絡先フォルダーの電子メール アドレスを迷惑メール ルールに追加し、ルールのセクションは NULL である必要があります。
  
このプロパティに値 "0x00000001" が指定されている場合、追加された連絡先に迷惑メール ルールの信頼できる連絡先セクションにまだ含まれていない電子メール アドレスがある場合は、これらの電子メール アドレスを制限に追加する必要があります。 このプロパティが "0x00000000"の場合、アクションは必要ありません。
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連するプロトコル仕様へのExchange Server提供します。
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> 許可/ブロック リストの処理と迷惑メール メッセージの決定を有効にできます。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
Mapitags.h
  
> 代替名として一覧表示されるプロパティの定義が含まれる。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

