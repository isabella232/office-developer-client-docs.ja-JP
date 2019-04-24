---
title: PidTagGender 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: '最終更新日時: 2015 年 3 月 9 日'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316157"
---
# <a name="pidtaggender-canonical-property"></a>PidTagGender 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージングユーザーの性別を含みます。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |PR_GENDER  <br/> |
|識別子:  <br/> |0x3a4d  <br/> |
|データの種類 :   <br/> |PT_I2  <br/> |
|エリア:  <br/> |MAPI メールユーザー  <br/> |
   
## <a name="remarks"></a>解説

このプロパティは、メッセージングユーザーおよびコンテンツに関する id とアクセス情報を提供します。 コンテンツは、メッセージングユーザーおよびメッセージングユーザーの組織によって定義されます。 
  
このプロパティに指定できる値は、性別列挙で定義されています。 これらは次のように一覧表示されます。
  
|**性別列挙**|**値**|**説明**|
|:-----|:-----|:-----|
|genderunspecified  <br/> |0x0000  <br/> |連絡先の性別が指定されていません。  <br/> |
|genderfemale  <br/> |0x0001  <br/> |連絡先は女性です。  <br/> |
|gendermale  <br/> |0x0002  <br/> |連絡先は男性です。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコル仕様への参照を提供します。
    
[[OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> 連絡先および個人用配布リストに対して許容されるプロパティと操作を指定します。
    
[[OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> ユーザー、連絡先、グループ、およびリソースのリストのプロパティと操作を指定します。
    
### <a name="header-files"></a>ヘッダーファイル

mapidefs.h
  
> データ型定義を提供します。
    
Mapitags
  
> 代替名としてリストされているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名から MAPI 名へのマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名から標準プロパティ名へのマッピング](mapping-mapi-names-to-canonical-property-names.md)

