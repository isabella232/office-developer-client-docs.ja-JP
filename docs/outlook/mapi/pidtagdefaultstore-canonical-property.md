---
title: PidTagDefaultStore の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefaultStore
api_type:
- HeaderDef
ms.assetid: 6314d91c-4948-4fd1-bacc-932d4bb2c22f
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 573ac849bba026ec6a5988220a7e49688393440d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802662"
---
# <a name="pidtagdefaultstore-canonical-property"></a>PidTagDefaultStore の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ ストアがメッセージ ストアのテーブルの既定のメッセージ ストアの場合、TRUE が格納されます。 
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_DEFAULT_STORE  <br/> |
|識別子:  <br/> |0x3400  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |MAPI メッセージ ストア  <br/> |
   
## <a name="remarks"></a>備考

このプロパティは、メッセージ ストアのテーブルの列として表示されます。 値は、 **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) に基づいています。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> 関連する Exchange Server プロトコルの仕様への参照を提供します。
    
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

