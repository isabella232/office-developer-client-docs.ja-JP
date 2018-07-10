---
title: PidTagImplicitConversionProhibited の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImplicitConversionProhibited
api_type:
- HeaderDef
ms.assetid: c6cb5a86-0105-4743-9f8e-b832e898da52
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: dcfaf9f4e71a13a8697da0cac98f7ea9cc3d8708
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802855"
---
# <a name="pidtagimplicitconversionprohibited-canonical-property"></a>PidTagImplicitConversionProhibited の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
メッセージ転送エージェント (MTA) が暗黙的なメッセージのテキストの変換をすることから禁止されている場合 TRUE が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_IMPLICIT_CONVERSION_PROHIBITED  <br/> |
|識別子:  <br/> |0x0016  <br/> |
|データを入力します。  <br/> |PT_BOOLEAN  <br/> |
|領域:  <br/> |Server  <br/> |
   
## <a name="remarks"></a>備考

このプロパティが TRUE の場合は、メッセージング システムする必要がありますで実行できません、コンテンツを変換、メッセージは、 **PR_EXPLICIT_CONVERSION** ([PidTagExplicitConversion](pidtagexplicitconversion-canonical-property.md)) プロパティを使用して受信者ごとの単位で明示的に要求された場合を除き。
  
## <a name="related-resources"></a>関連リソース

### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
Mapitags.h
  
> 関連付けられているプロパティとして記載されているプロパティの定義が含まれています。
    
## <a name="see-also"></a>関連項目



[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
