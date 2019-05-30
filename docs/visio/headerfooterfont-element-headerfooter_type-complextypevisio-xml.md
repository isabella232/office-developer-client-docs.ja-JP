---
title: HeaderFooterFont 要素 (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4e69dd4f-7281-e988-b1fd-93ac8c775c03
description: ヘッダーおよびフッターのテキストに使用されるフォントを指定します。
ms.openlocfilehash: b87ba96d551bf943dd330aa428f2c943c9d29269
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541086"
---
# <a name="headerfooterfont-element-headerfootertype-complextype-visio-xml"></a>HeaderFooterFont 要素 (HeaderFooter_Type complexType) (Visio XML)

ヘッダーおよびフッターのテキストに使用されるフォントを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |文書の xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="HeaderFooterFont" type="HeaderFooterFont_Type" minOccurs="0" maxOccurs="1" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[HeaderFooter](headerfooter-element-visiodocument_type-complextypevisio-xml.md) <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |文書のヘッダーとフッターの要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

なし。
  
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントの文字セットを指定します。 GDI Log/Tltlfcharset フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|ClipPrecision  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントのクリッピング精度を指定します。 GDI LOGFONTlfClipPrecision フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|実際  <br/> |xsd: int  <br/> |省略可能  <br/> |フォントの傾斜の属性を指定します。 GDI Log/Tltlf傾斜フィールドに相当します。  <br/> |Xsd: int 型の値。  <br/> |
|FaceName  <br/> |xsd: string  <br/> |省略可能  <br/> |フォントに関する情報を格納します。  <br/> |Xsd: string 型の値。  <br/> |
|Height  <br/> |xsd: int  <br/> |省略可能  <br/> |図形の高さを図面単位で指定します。  <br/> |Xsd: int 型の値。  <br/> |
|斜体  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントを斜体にするかどうかを指定します。 GDI Logフォント/斜体フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|Orientation  <br/> |xsd: int  <br/> |省略可能  <br/> |フォントの向きを指定します。 GDI Logの "GDI/メッセージ" フィールドに相当します。  <br/> |Xsd: int 型の値。  <br/> |
|アウト精度  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントの出力精度属性を指定します。 GDI Logの [出力精度] フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|PitchAndFamily  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントのピッチとファミリを指定します。 GDI LOGFONTlfPitchAndFamily フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|Quality  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントの出力品質を指定します。 GDI Logの [結果] フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|線  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントが取り消し線のフォントであるかどうかを指定します。 GDI Logの [結果] フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|下線  <br/> |xsd: アン Signedbyte  <br/> |省略可能  <br/> |フォントに下線を引かせるかどうかを指定します。 GDI Logの [/下線] フィールドに相当します。  <br/> |Xsd:/Signedbyte 型の値。  <br/> |
|太さ  <br/> |xsd: int  <br/> |省略可能  <br/> |フォントの太さを指定します。 GDI Logの [/重み] フィールドに相当します。  <br/> |Xsd: int 型の値。  <br/> |
|Width  <br/> |xsd: int  <br/> |省略可能  <br/> |関連付けられた図形の幅を図面単位で格納します。  <br/> |Xsd: int 型の値。  <br/> |
   

