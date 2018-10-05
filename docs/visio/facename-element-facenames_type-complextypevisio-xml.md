---
title: フォント名の要素 (FaceNames_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: フォントに関する情報が含まれています。
ms.openlocfilehash: 4c8f047d655be167dc058b3e29ac62161887ce99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389779"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>フォント名の要素 (FaceNames_Type complexType)'Visio XML (')

フォントに関する情報が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |**フォント名**の要素のコレクションが含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|文字集合  <br/> |xsd:string  <br/> |省略可能  <br/> |サポートされている文字のフォントを設定します。  <br/> |Xsd:string の値を入力します。  <br/> |
|Flags  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |次に示すフラグ: フォント、デフォルトのフォント、アジア言語のフォント、複雑なフォント、縦書きフォント、およびフォントの種類がありません。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |必須  <br/> |Utf-16 Unicode 文字列のフォントの名前。  <br/> ||
|Panos  <br/> |xsd:string  <br/> |省略可能  <br/> |フォントの panose 署名します。 Panose は、その視覚的特性に基づくに分類されている書体の分類システムです。  <br/> |Xsd:string の値を入力します。  <br/> |
|UnicodeRanges  <br/> |xsd:string  <br/> |省略可能  <br/> |フォントのサポートされている Unicode の範囲です。  <br/> |Xsd:string の値を入力します。  <br/> |
   

