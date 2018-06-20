---
title: PidTagUserFields の標準的なプロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: '�ŏI�X�V��: 2015�N3��9��'
ms.openlocfilehash: 5abfd9c98c5a83ca45792f094d0c9573b8affb85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19803653"
---
# <a name="pidtaguserfields-canonical-property"></a>PidTagUserFields の標準的なプロパティ

  
  
**適用されます**: Outlook 
  
名前、データ型、およびその他のユーザー定義のフィールド情報が含まれています。
  
|||
|:-----|:-----|
|関連するプロパティ。  <br/> |PR_USERFIELDS  <br/> |
|識別子:  <br/> |0x36E3  <br/> |
|データを入力します。  <br/> |PT_BINARY  <br/> |
|領域:  <br/> |MAPI フォルダー  <br/> |
   
## <a name="remarks"></a>備考

、各項目については、Outlook は、対応する**IMessage**オブジェクトの[PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md)プロパティにユーザー定義のすべてのフィールドの定義を格納します。 **PidLidPropertyDefinitionStream**プロパティには、 [PropertyDefinition](propertydefinition-stream-structure.md)、フィールド定義が含まれていると呼ばれるバイナリ ストリームが含まれています。 ストリームの構造体フィールドの定義の詳細については、[ストリームの構造](stream-structures.md)を参照してください。
  
フォルダーごとには、Outlook は、関連付けられたメッセージのメッセージ クラスの IPC.MS の**PidTagUserFields**プロパティには、そのフォルダー内のすべてのユーザー定義フィールドの定義を格納します。REN。USERFIELDS の各フォルダーはその内容が関連付けられているテーブルでは、このクラスの複数のメッセージが含まれていると推定します。 
  
> [!NOTE]
> フォルダー内のユーザー定義フィールドのセットは可能性があります必ずしもその項目の各フィールドのユーザー定義の設定を一致しません。 
  
一連のフォルダー内のユーザー定義フィールドは、フォルダーの [フィールドの選択など、Outlook の UI でのさまざまな場所に表示されます。 メッセージの**PidTagUserFields**プロパティには、バイナリ ストリーム、 **FolderUserFields**、フォルダー フィールドの定義が含まれているが含まれています。 フォルダー フィールドの定義については、ストリームの構造体の詳細については、[フォルダー フィールドのストリームの構造体](folder-fields-stream-structures.md)および[FolderUserFields ストリームのサンプル](folderuserfields-stream-sample.md)を参照してください。
  
## <a name="section-heading"></a>セクションの見出し

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

