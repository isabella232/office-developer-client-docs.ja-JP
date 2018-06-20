---
title: ページ要素 (Pages_Type complexType)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: ドキュメント内のページを定義する要素が含まれています。
ms.openlocfilehash: 368c50a25a09d5f4fd808f3f019b074b7f6d246d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805945"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>ページ要素 (Pages_Type complexType)'Visio XML (')

ドキュメント内のページを定義する要素が含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |ドキュメントの**ページ**要素が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |**ページ**要素のページ シートを定義する要素が含まれています。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|背景  <br/> |xsd:boolean  <br/> |省略可能  <br/> |ページが背景ページであることを示すフラグです。  <br/> |Xsd:boolean の値を入力します。  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |このページの背景ページの ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |必須  <br/> |その親要素内の要素の一意の ID。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |省略可能  <br/> |名前がユーザーによってカスタマイズされているかどうかを示します。  <br/> |Xsd:Boolean の値を入力します。  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |省略可能  <br/> |汎用名がユーザーによってカスタマイズされているかどうかを示します。  <br/> |Xsd:Boolean の値を入力します。  <br/> |
|名前  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の名前です。  <br/> |Xsd:string の値を入力します。  <br/> |
|NameU  <br/> |xsd:string  <br/> |省略可能  <br/> |要素の汎用名です。  <br/> |Xsd:string の値を入力します。  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |省略可能  <br/> |校正用オーバーレイに関連付けられている校閲者の ID です。  <br/> |Xsd:unsignedInt の値を入力します。  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX**と**ViewCenterY**は、新しいビュー (ウィンドウ) には、最初に開いたときのページで中心点を指定します。  <br/> |Xsd:double 型の値です。  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |省略可能  <br/> |**ViewCenterX**と**ViewCenterY**は、新しいビュー (ウィンドウ) には、最初に開いたときのページで中心点を指定します。  <br/> |Xsd:double 型の値です。  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |省略可能  <br/> |ページの新しいビュー (ウィンドウ) を開くときに使用する既定の拡大率。 たとえば、1 は 100% です。1.5 = 150% というようにします。  <br/> |Xsd:double 型の値です。  <br/> |
   

