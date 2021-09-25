---
title: Data1 要素 (ShapeSheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d72dc0e4-4e0f-dd3f-a51a-8486f9ec548e
description: 図形に関する追加情報を提供するために使用される任意の文字列値を含む。
ms.openlocfilehash: f3432bcb1fff7245bf3f579c17db42cf43e3f6a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582898"
---
# <a name="data1-element-shapesheet_type-complextype-visio-xml"></a>Data1 要素 (ShapeSheet_Type complexType) (Visio XML)

図形に関する追加情報を提供するために使用される任意の文字列値を含む。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Data1" type="Data_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |**Master、Page、** またはグループ図形要素で図形を定義する要素を含む。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

なし。
  

