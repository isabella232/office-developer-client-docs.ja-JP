---
title: Trigger 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Microsoft Visioに、Visio ファイル内のドキュメント パーツ間のリレーションシップを再計算するVisioします。
ms.openlocfilehash: c6223107182862df0772316dab2218dbf6180fae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549456"
---
# <a name="trigger-element-visio-xml"></a>Trigger 要素 (Visio XML)

Microsoft Visioに、Visio ファイル内のドキュメント パーツ間のリレーションシップを再計算するVisioします。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形の定義に関する情報を提供するセル要素を指定します。  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |DocumentSheet 構造を定義します。  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |図面で定義されているスタイルを表します。  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |マスターに関連付けられた図面ページのプロパティを指定します。  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面ページに関連付けられている図面ページのプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面内の参照参照ページを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |必須  <br/> |トリガーのアクティブ化時に呼び出される数式の名前。  <br/> 「備考」セクションを参照してください。  <br/> |xsd:string 型の値。  <br/> |
   
## <a name="remarks"></a>注釈

この **Trigger 要素** の **N** 属性は、トリガー命令に対応する制限された値のセットの 1 つである必要があります。 この Trigger 要素で許可されている **N** 属性の値を決定するには、以下の表を **参照** してください。 
  
|**値**|**親要素**|**説明**|
|:-----|:-----|:-----|
|CategoryChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**HASCATEGORIES** 関数を使用したクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**BKGPAGENAME** 関数を使用したクロスパーツ参照が存在するときにページに表示されるトリガー  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |ページまたはページに含まれる図形が RGB 関数を使用するたびにページに表示される **トリガー** 。  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCCREATION** 関数を使用したクロスパーツ参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |DATA1 関数を使用したクロスパーツ参照が存在するときに図形に **表示される** トリガー。  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA2** 関数を使用したクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA3** 関数を使用したクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |DOCLASTEDIT 関数を使用したクロスパーツ参照が存在する場合にドキュメント **に表示される** トリガー。  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |ID 関数を使用したクロスパーツ参照が存在するときに図形に表示される **トリガー** 。  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**MASTERNAME** 関数を使用したクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |NAME 関数を使用したクロスパーツ参照が存在するときに図形に表示 **されるトリガー** 。  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |ページまたはページに含まれる図形に **NOW** 関数または **RAND** 関数が含まれている場合に、ページに表示されるトリガー。  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**PAGECOUNT** 関数を使用したクロスパーツ参照が存在するときにドキュメントに表示されるトリガー。  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**PAGENAME** 関数を使用したクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |PAGENUMBER 関数を使用したクロスパーツ参照が存在する場合にページに表示 **されるトリガー** 。  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**POINTALONGPATH、PATHLENGTH、または** **PATHSEGMENT** 関数を使用するクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTPRINT** 関数を使用したクロスパーツ参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTSAVE** 関数を使用したクロスパーツ参照が存在するときにドキュメントに表示されるトリガー。  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |CATEGORY、CREATOR、DESCRIPTION、KEYWORDS、SUBJECT、または TITLE 関数を使用するクロスパーツ参照が存在する場合にドキュメントに表示される **トリガー** 。   <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |TYPE 関数を使用したクロスパーツ参照が存在するときに図形に表示 **されるトリガー** 。  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**CONTAINERMEMBERCOUNT** 関数を使用したクロスパーツ参照が存在するときに図形に表示されるトリガー。  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**CONTAINERSHEETREF** 関数を使用するクロスパーツ参照が存在する場合にページに表示されるトリガー。  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**POINTALONGPATH、PATHLENGTH、または** **PATHSEGMENT** 関数を使用するクロスパーツ参照が存在するときにページに表示されるトリガー。  <br/> |
   

