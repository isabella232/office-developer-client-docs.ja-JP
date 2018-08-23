---
title: HeaderFooterFont 要素 (HeaderFooter_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: ヘッダーおよびフッターのテキストに使用するフォントを指定します。
ms.openlocfilehash: 249040702b1594cc650ccf1304ed7c1c79581ea3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805507"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>HeaderFooterFont 要素 (HeaderFooter_Type complexType)'Visio XML (')

ヘッダーおよびフッターのテキストに使用するフォントを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |ドキュメントのヘッダーとフッターの要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|文字セット  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントの文字セットを指定します。 GDI の LOGFONTlfCharSet フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントのクリッピング精度を指定します。 GDI の LOGFONTlfClipPrecision フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|文字送り  <br/> |xsd:int  <br/> |省略可能  <br/> |フォントの傾斜の属性を指定します。 GDI の LOGFONTlfEscapement フィールドと等価です。  <br/> |Xsd:int 型の値です。  <br/> |
|フォント名  <br/> |xsd:string  <br/> |省略可能  <br/> |フォントに関する情報が含まれています。  <br/> |Xsd:string の値を入力します。  <br/> |
|Height  <br/> |xsd:int  <br/> |省略可能  <br/> |図面の単位で図形の高さを指定します。  <br/> |Xsd:int 型の値です。  <br/> |
|イタリック  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントが斜体かどうかを指定します。 GDI の LOGFONTlfItalic フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|オリエンテーション  <br/> |xsd:int  <br/> |省略可能  <br/> |フォントの向きを指定します。 GDI の LOGFONTlfOrientation フィールドと等価です。  <br/> |Xsd:int 型の値です。  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントの出力精度の属性を指定します。 GDI の LOGFONTlfOutPrecision フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |ピッチとファミリのフォントを指定します。 GDI の LOGFONTlfPitchAndFamily フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|品質  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントの出力品質を指定します。 GDI の LOGFONTlfQuality フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|取り消し線  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントが取り消し線のフォントかどうかを指定します。 GDI の LOGFONTlfStrikeOut フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|下線  <br/> |xsd:unsignedByte  <br/> |省略可能  <br/> |フォントが下線付きかどうかを指定します。 GDI の LOGFONTlfUnderline フィールドと等価です。  <br/> |Xsd:unsignedByte の値を入力します。  <br/> |
|太さ  <br/> |xsd:int  <br/> |省略可能  <br/> |フォントの太さを指定します。 GDI の LOGFONTlfWeight フィールドと等価です。  <br/> |Xsd:int 型の値です。  <br/> |
|Width  <br/> |xsd:int  <br/> |省略可能  <br/> |図面の単位に関連付けられている図形の幅が含まれています。  <br/> |Xsd:int 型の値です。  <br/> |
   

