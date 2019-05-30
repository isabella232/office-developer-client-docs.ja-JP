---
title: Trigger 要素 (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Visio ファイル内の文書パーツ間のリレーションシップを再計算するための手順を Microsoft Visio に提供します。
ms.openlocfilehash: e757331984586dc910ada7d14e6385761f15929f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542906"
---
# <a name="trigger-element-visio-xml"></a>Trigger 要素 (Visio XML)

Visio ファイル内の文書パーツ間のリレーションシップを再計算するための手順を Microsoft Visio に提供します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |マスター # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形の定義に関する情報を提供する cell 要素を指定します。  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |DocumentSheet の構造を定義します。  <br/> |
|[Xsl](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |図面で定義されているスタイルを表します。  <br/> |
|[PageSheet (Master_Type complexType)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |マスターシェイプに関連付けられている図面ページのプロパティを指定します。  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面ページに関連付けられた図面ページのプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面内の文献の参照ページを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd: string  <br/> |必須  <br/> |トリガーがアクティブ化されたときに呼び出される式の名前を指定します。  <br/> 「備考」セクションを参照してください。  <br/> |Xsd: string 型の値。  <br/> |
   
## <a name="remarks"></a>注釈

この**トリガ**要素の**N**属性は、トリガ命令に対応する制限された値のセットのいずれかである必要があります。 この**Trigger**要素で許可されている**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**親要素**|**説明**|
|:-----|:-----|:-----|
|変更されたカテゴリ  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**Hascategories**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**BKGPAGENAME**関数を使用したパート間参照が存在する場合にページに表示されるトリガー  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |ページまたはその中に含まれている図形のいずれかに**RGB**関数を使用している場合に、ページに表示されるトリガー。  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**Doccreation**関数を使用したパート間参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA1**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA2**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA3**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTEDIT**関数を使用したパート間参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**ID**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**Mastername**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**NAME**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |ページまたはその中に含まれる図形のいずれかが**NOW**または**RAND**関数を持つ場合に、ページに表示されるトリガー。  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**PAGECOUNT**関数を使用したパート間参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**PAGENAME**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**PAGENUMBER**関数を使用したパート間参照が存在する場合に、ページに表示されるトリガー。  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**POINTALONGPATH**、 **pathlength**、または**pathlength**関数を使用したパート間参照が存在する場合に、図形に表示されるトリガー。  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTPRINT**関数を使用したパート間参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTSAVE**関数を使用したパート間参照が存在する場合にドキュメントに表示されるトリガー。  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**CATEGORY**、 **CREATOR**、 **DESCRIPTION**、 **KEYWORDS**、 **SUBJECT**、 **TITLE**の各関数を使用したパート間参照が存在する場合に、ドキュメントに表示されるトリガー。  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**TYPE**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**CONTAINERMEMBERCOUNT**関数を使用したパート間参照が存在する場合に図形に表示されるトリガー。  <br/> |
|[Zorderchanged]  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**CONTAINERSHEETREF**関数を使用したパート間参照が存在する場合に、ページに表示されるトリガー。  <br/> |
|パス  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**POINTALONGPATH**、 **pathlength**、または**pathlength**関数を使用したパート間参照が存在する場合に、ページに表示されるトリガー。  <br/> |
   

