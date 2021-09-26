---
title: FooterMargin 要素 (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 047f42cf-4202-50bd-40b4-a71052e2dfb3
description: ドキュメントのフッターの余白を指定します。
ms.openlocfilehash: a0a6e1b8d94d29d901e260325e00d295a4f9ad3f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598669"
---
# <a name="footermargin-element-headerfooter_type-complextype-visio-xml"></a>FooterMargin 要素 (HeaderFooter_Type complexType) (Visio XML)

ドキュメントのフッターの余白を指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[FooterMargin_Type](footermargin_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="FooterMargin" type="FooterMargin_Type" minOccurs="0" maxOccurs="1" >
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
|単位  <br/> |xsd:string  <br/> |省略可能  <br/> |単位を表します。 既定値は IN です。  <br/> |xsd:string 型の値。  <br/> |
   

