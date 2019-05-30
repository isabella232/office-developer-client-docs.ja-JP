---
title: FaceName 要素 (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: フォントに関する情報を格納します。
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541016"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>FaceName 要素 (FaceNames_Type complexType) (Visio XML)

フォントに関する情報を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書の xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[FaceNames 方法](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |**Facename**要素のコレクションを格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |xsd: string  <br/> |省略可能  <br/> |フォントのサポートされている文字セット。  <br/> |Xsd: string 型の値。  <br/> |
|フラグ  <br/> |xsd: アン Signedint  <br/> |省略可能  <br/> |無効なフォント、既定のフォント、アジア言語のフォント、コンプレックスフォント、縦書きフォント、およびフォントの種類を示すフラグ。  <br/> |Xsd:/Signedint 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |必須  <br/> |UTF-16 Unicode 文字列としてのフォントの名前。  <br/> ||
|Panos  <br/> |xsd: string  <br/> |省略可能  <br/> |フォントの panose シグネチャ。 Panose は、視覚特性に基づいて分類される書体システムです。  <br/> |Xsd: string 型の値。  <br/> |
|UnicodeRanges  <br/> |xsd: string  <br/> |省略可能  <br/> |サポートされているフォントの範囲。  <br/> |Xsd: string 型の値。  <br/> |
   

