---
title: FaceName 要素 (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: フォントに関する情報が含まれる。
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541016"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>FaceName 要素 (FaceNames_Type complexType) (Visio XML)

フォントに関する情報が含まれる。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |FaceName 要素のコレクション **を含** む。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd:string  <br/> |省略可能  <br/> |サポートされているフォントの文字セット。  <br/> |xsd:string 型の値。  <br/> |
|フラグ  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |不足しているフォント、既定のフォント、アジアのフォント、複雑なフォント、垂直フォント、およびフォントの種類を示すフラグ。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|NameU  <br/> |xsd:string  <br/> |必須  <br/> |フォントの名前を UTF-16 Unicode 文字列として指定します。  <br/> ||
|Panos  <br/> |xsd:string  <br/> |省略可能  <br/> |フォントのパノセシグニチャ。 Panose は、視覚的特性に基づいて分類する書体の分類システムです。  <br/> |xsd:string 型の値。  <br/> |
|UnicodeRanges  <br/> |xsd:string  <br/> |省略可能  <br/> |サポートされているフォントの Unicode 範囲。  <br/> |xsd:string 型の値。  <br/> |
   

