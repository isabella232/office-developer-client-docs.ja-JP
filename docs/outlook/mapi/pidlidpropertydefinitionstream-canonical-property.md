---
title: PidLidPropertyDefinitionStream 標準プロパティ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidLidPropertyDefinitionStream
api_type:
- COM
ms.assetid: ead35049-e60e-4b46-bf12-f73d77cd36b2
description: '最終更新日: 2015 年 3 月 9 日'
ms.openlocfilehash: 2ba6fc19d52e0dbc54c863e0906bf8ff56b512a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616678"
---
# <a name="pidlidpropertydefinitionstream-canonical-property"></a>PidLidPropertyDefinitionStream 標準プロパティ

  
  
**適用対象**: Outlook 2013 | Outlook 2016 
  
メッセージの組み込みフィールドのユーザー定義フィールドとデータ バインド設定の定義を表します。
  
|||
|:-----|:-----|
|関連するプロパティ:  <br/> |dispidPropDefStream  <br/> |
|プロパティ セット:  <br/> |PSETID_Common  <br/> |
|長い ID (LID):  <br/> |0x00008540  <br/> |
|データの種類 :   <br/> |PT_BINARY  <br/> |
|エリア:  <br/> |実行時の構成  <br/> |
   
## <a name="remarks"></a>注釈

**PidLidPropertyDefinitionStream** プロパティの値は、メッセージのカスタム フォーム定義の一部として保存されます。 
  
このプロパティの値はバイナリ ストリームです。 このストリームの構造については [、「PropertyDefinition Stream Structure」を参照してください](propertydefinition-stream-structure.md)。 
  
## <a name="related-resources"></a>関連リソース

### <a name="protocol-specifications"></a>プロトコルの仕様

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> プロパティ セットの定義と、関連するプロトコル仕様へのExchange Serverを提供します。
    
### <a name="header-files"></a>ヘッダー ファイル

Mapidefs.h
  
> データ型の定義を提供します。
    
## <a name="see-also"></a>関連項目



[Outlookアイテムとフィールド](outlook-items-and-fields.md)
  
[新しいフィールドの定義をUser-Definedする](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[PropertyDefinition ストリームのサンプル](propertydefinition-stream-sample.md)
  
[MAPI のプロパティ](mapi-properties.md)
  
[MAPI 標準プロパティ](mapi-canonical-properties.md)
  
[標準プロパティ名を MAPI 名にマッピングする](mapping-canonical-property-names-to-mapi-names.md)
  
[MAPI 名を標準プロパティ名にマッピングする](mapping-mapi-names-to-canonical-property-names.md)

