---
title: HeaderFooterFont 要素 (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: ヘッダーおよびフッターのテキストに使用されるフォントを指定します。
ms.openlocfilehash: a862141d12234efeaecdfe6976a1c19f18cbe6ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574154"
---
# <a name="headerfooterfont-element-headerfooter_type-complextype-visio-xml"></a>HeaderFooterFont 要素 (HeaderFooter_Type complexType) (Visio XML)

ヘッダーおよびフッターのテキストに使用されるフォントを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |ドキュメントのヘッダーとフッターの要素を含む。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントの文字セットを指定します。 GDI LOGFONTlfCharSet フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントのクリッピング精度を指定します。 GDI LOGFONTlfClipPrecision フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|Escapement  <br/> |xsd:int  <br/> |省略可能  <br/> |フォントのエスケープメント属性を指定します。 GDI LOGFONTlfEscapement フィールドと同じです。  <br/> |xsd:int 型の値。  <br/> |
|FaceName  <br/> |xsd:string  <br/> |省略可能  <br/> |フォントに関する情報が含まれる。  <br/> |xsd:string 型の値。  <br/> |
|Height  <br/> |xsd:int  <br/> |省略可能  <br/> |図形の高さを図面単位で指定します。  <br/> |xsd:int 型の値。  <br/> |
|斜体  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントが italic かどうかを指定します。 GDI LOGFONTlfItalic フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|Orientation  <br/> |xsd:int  <br/> |省略可能  <br/> |フォントの向きを指定します。 GDI LOGFONTlfOrientation フィールドと同じです。  <br/> |xsd:int 型の値。  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントの出力精度属性を指定します。 GDI LOGFONTlfOutPrecision フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントのピッチとファミリを指定します。 GDI LOGFONTlfPitchAndFamily フィールドに相当します。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|品質  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントの出力品質を指定します。 GDI LOGFONTlfQuality フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントが取り消し線フォントかどうかを指定します。 GDI LOGFONTlfStrikeOut フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|下線  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントに下線が付くかどうかを指定します。 GDI LOGFONTlfUnderline フィールドと同じです。  <br/> |xsd:unsignedByte 型の値。  <br/> |
|太さ  <br/> |xsd:int  <br/> |省略可能  <br/> |フォントの重みを指定します。 GDI LOGFONTlfWeight フィールドと同じです。  <br/> |xsd:int 型の値。  <br/> |
|Width  <br/> |xsd:int  <br/> |省略可能  <br/> |図面単位で関連付けられた図形の幅を格納します。  <br/> |xsd:int 型の値。  <br/> |
   

