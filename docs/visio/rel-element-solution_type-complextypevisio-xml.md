---
title: Rel 要素 (Solution_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8438fe4b-f5f7-d4e4-58b7-7ebdc1da197a
description: このソリューションに関連付けられているソリューション XML を使用してパーツへのリレーションシップを指定します。
ms.openlocfilehash: e8a1350691e8d29551fb126a2151655175cc068c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320014"
---
# <a name="rel-element-solutiontype-complextype-visio-xml"></a>Rel 要素 (Solution_Type complexType) (' Visio XML ')

このソリューションに関連付けられているソリューション XML を使用してパーツへのリレーションシップを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |system.xml、masters、config.xml、pages、page # .xml、.master (.xml)  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="Rel" type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Solution](solution-element-solutions_type-complextypevisio-xml.md) <br/> |[Solution_Type](solution_type-complextypevisio-xml.md) <br/> |図面に格納されているソリューション XML の1つのインスタンスを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|r: id  <br/> |xsd: string  <br/> 注釈を参照してください。  <br/> |必須  <br/> |パーツへのリレーションシップを指定します。  <br/> |"rId #"  <br/> 注釈を参照してください。  <br/> |
   
## <a name="remarks"></a>解説

**r: id**属性の値は、 **ST_RelationshipID**型でなければなりません。 **ST_RelationshipID** type は、' rId # ' という形式で指定する必要があります。最後の文字は数字である必要があります。 この数値は、 **Rel**要素のすべての兄弟要素の間で一意である必要があります。 
  
ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 Part 1 の仕様](https://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。
  

