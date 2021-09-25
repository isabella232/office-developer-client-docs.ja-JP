---
title: Page 要素 (Pages_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: ドキュメント内のページを定義する要素が含まれます。
ms.openlocfilehash: acdc74fa35480dccdd240030e59eafd57114b080
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573797"
---
# <a name="page-element-pages_type-complextype-visio-xml"></a>Page 要素 (Pages_Type complexType) (Visio XML)

ドキュメント内のページを定義する要素が含まれます。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |ドキュメントの **Page** 要素を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Page 要素のページ シートを定義する要素が **含** まれます。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|背景  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ページが背景ページかどうかを示すフラグ。  <br/> |xsd:boolean 型の値。  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このページの背景ページの ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |親要素内の要素の一意の ID です。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |名前がユーザーによってカスタマイズされているかどうかを示します。  <br/> |xsd:Boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ユニバーサル名がユーザーによってカスタマイズされているかどうかを示します。  <br/> |xsd:Boolean 型の値。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd:string 型の値。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd:string 型の値。  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |マークアップ オーバーレイに関連付けられたレビューアーの ID。  <br/> |xsd:unsignedInt 型の値。  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX** および **ViewCenterY** では、新しいビュー (ウィンドウ) が最初に開いたときに想定されるページ上の中心点を指定します。  <br/> |xsd:double 型の値。  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX** および **ViewCenterY** では、新しいビュー (ウィンドウ) が最初に開いたときに想定されるページ上の中心点を指定します。  <br/> |xsd:double 型の値。  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |省略可能  <br/> |ページの新しいビュー (ウィンドウ) を開くときに使用する既定の拡大率です。 たとえば、1 = 100%、1.5 = 150% などです。  <br/> |xsd:double 型の値。  <br/> |
   

