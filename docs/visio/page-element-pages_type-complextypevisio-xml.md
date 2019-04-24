---
title: Page 要素 (Pages_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: 文書内のページを定義する要素を格納します。
ms.openlocfilehash: 800e4ab2c6446ab298747f0492800000bb44cca3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334448"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Page 要素 (Pages_Type complexType) (' Visio XML ')

文書内のページを定義する要素を格納します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |ページの xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |文書の**ページ**要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |**page**要素のページシートを定義する要素を格納します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|背景  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ページが背景ページかどうかを示すフラグ。  <br/> |xsd: boolean 型の値。  <br/> |
|BackPage  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |このページの背景ページの ID です。  <br/> |xsd:/signedint 型の値。  <br/> |
|ID  <br/> |xsd: アン signedint  <br/> |必須  <br/> |親要素内の要素の一意の ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|iscustomname  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーによって名前がカスタマイズされているかどうかを示します。  <br/> |xsd: Boolean 型の値。  <br/> |
|IsCustomNameU  <br/> |xsd: boolean  <br/> |省略可能  <br/> |ユーザーが汎用名をカスタマイズしたかどうかを示します。  <br/> |xsd: Boolean 型の値。  <br/> |
|名前  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の名前。  <br/> |xsd: string 型の値。  <br/> |
|NameU  <br/> |xsd: string  <br/> |省略可能  <br/> |要素の汎用名。  <br/> |xsd: string 型の値。  <br/> |
|ReviewerID  <br/> |xsd: アン signedint  <br/> |省略可能  <br/> |マークアップオーバーレイに関連付けられているレビュー担当者の ID。  <br/> |xsd:/signedint 型の値。  <br/> |
|ViewCenterX  <br/> |xsd: double  <br/> |省略可能  <br/> |**ViewCenterX**および**viewcenter y**では、最初に開いたときに新しいビュー (ウィンドウ) が想定するページ上の中心点を指定します。  <br/> |xsd: double 型の値。  <br/> |
|view中央 y  <br/> |xsd: double  <br/> |省略可能  <br/> |**ViewCenterX**および**viewcenter y**では、最初に開いたときに新しいビュー (ウィンドウ) が想定するページ上の中心点を指定します。  <br/> |xsd: double 型の値。  <br/> |
|viewscale  <br/> |xsd: double  <br/> |省略可能  <br/> |ページの新しいビュー (ウィンドウ) を開くときに使用する既定の拡大率を設定します。 たとえば、1 = 100% のようにします。1.5 = 150% など。  <br/> |xsd: double 型の値。  <br/> |
   

