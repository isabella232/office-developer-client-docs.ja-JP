---
title: PidTagGender の標準的なプロパティ
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
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: b2ac7aa4fca8583fc59d727c55433108bee62dee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802808"
---
# <a name="pidtaggender-canonical-property"></a>PidTagGender の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージング ユーザーの性別が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_GENDER  <br/> |
|識別子:  <br/> |0x3A4D  <br/> |
|データを入力します。  <br/> |PT_I2  <br/> |
|領域:  <br/> |MAPI メール ユーザー  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、id およびメッセージングのユーザーに関する情報にアクセスを提供し、コンテンツは。 コンテンツは、メッセージングのユーザーとメッセージのユーザーの組織によって定義されます。 
  
このプロパティの有効な値は、性別の列挙体で定義されます。 これらは以下のとおり。
  
|**性別の列挙**|**値**|**説明**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |連絡先の性別が指定されていません。  <br/> |
|genderFemale  <br/> |0x0001  <br/> |連絡先は、(メス) です。  <br/> |
|genderMale  <br/> |0x0002  <br/> |連絡先は、(オス) です。  <br/> |
   
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
[[MS OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> プロパティは、連絡先、個人用配布リストの許可の操作を指定します。
    
[[MS OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> プロパティとユーザー、連絡先、グループ、およびリソースのリストの操作を指定します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 代替名として記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)

