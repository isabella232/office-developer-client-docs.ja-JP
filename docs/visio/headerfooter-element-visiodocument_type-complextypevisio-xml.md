---
title: HeaderFooter 要素 (VisioDocument_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 026926cf-3d0b-984c-897e-9d28346b7ba7
description: ドキュメントのヘッダーとフッターの要素が含まれています。
ms.openlocfilehash: e5933ad318b8100569046668e3cc372ce9a03788
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805521"
---
# <a name="headerfooter-element-visiodocumenttype-complextype-visio-xml"></a>HeaderFooter 要素 (VisioDocument_Type complexType)'Visio XML (')

ドキュメントのヘッダーとフッターの要素が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[HeaderFooter_Type](headerfooter_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="HeaderFooter" type="HeaderFooter_Type" minOccurs="0" maxOccurs="1" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[VisioDocument](visiodocument-elementvisio-xml.md) <br/> |[VisioDocument_Type](visiodocument_type-complextypevisio-xml.md) <br/> |Microsoft Visio ドキュメントのルート要素です。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[中央](footercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterCenter_Type](footercenter_type-complextypevisio-xml.md) <br/> |図面のフッターの中央の部分に表示されるテキスト文字列が含まれています。  <br/> |
|[FooterLeft](footerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterLeft_Type](footerleft_type-complextypevisio-xml.md) <br/> |図面のフッターの左部分に表示されるテキスト文字列が含まれています。  <br/> |
|[FooterMargin](footermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterMargin_Type](footermargin_type-complextypevisio-xml.md) <br/> |図面のフッターの余白を指定します。  <br/> |
|[フッター](footerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[FooterRight_Type](footerright_type-complextypevisio-xml.md) <br/> |図面のフッターの右側に表示されるテキスト文字列が含まれています。  <br/> |
|[HeaderCenter](headercenter-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderCenter_Type](headercenter_type-complextypevisio-xml.md) <br/> |図面のヘッダーの中央の部分に表示されるテキスト文字列が含まれています。  <br/> |
|[HeaderFooterFont](headerfooterfont-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderFooterFont_Type](headerfooterfont_type-complextypevisio-xml.md) <br/> |ヘッダーおよびフッターのテキストに使用するフォントを指定します。  <br/> |
|[HeaderLeft](headerleft-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderLeft_Type](headerleft_type-complextypevisio-xml.md) <br/> |図面のヘッダーの左側の部分に表示されるテキスト文字列が含まれています。  <br/> |
|[HeaderMargin](headermargin-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderMargin_Type](headermargin_type-complextypevisio-xml.md) <br/> |図面のヘッダーの余白を指定します。  <br/> |
|[HeaderRight](headerright-element-headerfooter_type-complextypevisio-xml.md) <br/> |[HeaderRight_Type](headerright_type-complextypevisio-xml.md) <br/> |図面のヘッダーの右側の部分に表示されるテキスト文字列が含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|HeaderFooterColor  <br/> |xsd:string  <br/> |省略可能  <br/> |ヘッダーとフッターを 16 進表記でのテキストの色の RGB 値たとえば、#rrggbb です。  <br/> |Xsd:string の値を入力します。  <br/> |
   

