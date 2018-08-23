---
title: Rel の要素 (Master_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 151cdd13-d00b-249c-7ebd-1ae9c4042b03
description: 対応するマスター XML パーツへのリレーションシップを指定します。
ms.openlocfilehash: 8cd16c55b24cd6edec993cb913709beff72ee325
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806177"
---
# <a name="rel-element-mastertype-complextype-visio-xml"></a>Rel の要素 (Master_Type complexType)'Visio XML (')

対応するマスター XML パーツへのリレーションシップを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |pages.xml、masters.xml、recordsets.xml、ページ番号の .xml、マスター # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Rel"  type="Rel_Type" minOccurs="1" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Master](master-element-masters_type-complextypevisio-xml.md) <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |図面に格納されている XML をマスターの 1 つのインスタンスを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|r: id  <br/> |xsd:string  <br/> 注釈を参照してください。  <br/> |必須  <br/> |パーツへのリレーションシップを指定します。  <br/> |「# を削除する」  <br/> 注釈を参照してください。  <br/> |
   
## <a name="remarks"></a>注釈

**R: id**属性の値は、 **ST_RelationshipID**型である必要があります。 **ST_RelationshipID**型は、文字列形式にする必要がある 'rId #'、最後の文字がいくつかをする必要があります。 数は、 **Rel**の要素のすべての兄弟要素間で一意である必要があります。 
  
ST_RelationshipID 型の詳細については、 [ISO/IEC 29500 の第 1 部の仕様](http://www.iso.org/iso/home/store/catalogue_tc/catalogue_detail.md?csnumber=61750)を参照してください。
  

