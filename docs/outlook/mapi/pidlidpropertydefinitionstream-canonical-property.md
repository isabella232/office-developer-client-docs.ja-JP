---
title: PidLidPropertyDefinitionStream の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: f7f764d95c2fc36ba6af617333cb47d266cd2aa9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19802092"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>PidLidPropertyDefinitionStream の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
ユーザー定義のフィールドの定義と、メッセージの組み込みのフィールドのデータ バインディングの設定を表します。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |dispidPropDefStream  <br/> |
|プロパティを設定します。  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008540  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>備考

**PidLidPropertyDefinitionStream**プロパティの値は、メッセージのユーザー設定フォームの定義の一部として保存されます。 
  
このプロパティの値は、バイナリ ストリームです。 このストリームの構造については、 [PropertyDefinition ストリームの構造体](propertydefinition-stream-structure.md)を参照してください。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と関連する Exchange Server プロトコルの仕様への参照を提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型定義を提供します。
    
## <a name="see-also"></a>関連項目



[Outlook アイテムおよびフィールド](outlook-items-and-fields.md)
  
[新しいユーザー定義フィールドの定義を追加します。](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[MAPI プロパティ](mapi-properties.md)
  
[標準の MAPI プロパティ](mapi-canonical-properties.md)
  
[MAPI 名への標準的なプロパティ名のマッピング](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名前を標準のプロパティ名にマップします。](mapping-mapi-names-to-canonical-property-names.md)
