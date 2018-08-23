---
title: PageSheet 要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 824fbeb0-1a2f-35a0-50e3-c57143dc21ab
description: マスターに関連付けられている図面ページのプロパティを指定します。
ms.openlocfilehash: ab20cfe4561cd5fd0eeb6edad0b3a608428b0e8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806008"
---
# <a name="pagesheet-element-mastertype-complextype-visio-xml"></a>PageSheet 要素 (Master_Type complexType)'Visio XML (')

マスターに関連付けられている図面ページのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="PageSheet" type="PageSheet_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |図面のマスター シェイプを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |塗りつぶしの書式設定を継承するスタイル シートの ID を指定します。 図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |線の書式設定を継承するスタイル シートの ID を指定します。 図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |テキストの書式設定を継承するスタイル シートの ID を指定します。 図面内の**StyleSheet_Type**に関連付けられている**ID**属性の値である必要があります。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |省略可能  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:string の値を入力します。  <br/> |
   

