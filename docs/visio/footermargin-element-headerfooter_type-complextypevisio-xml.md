---
title: FooterMargin 要素 (HeaderFooter_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 047f42cf-4202-50bd-40b4-a71052e2dfb3
description: ドキュメントのフッターの余白を指定します。
ms.openlocfilehash: 5a147dbb8b94d9077836cb2269dd2ff72dae3b3a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538663"
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
   

