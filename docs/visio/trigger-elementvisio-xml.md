---
title: トリガー要素 ' Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d897d2d1-25ba-48d7-b87e-d3c533d88c15
description: Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。
ms.openlocfilehash: a590ec1f9c19270f75d4d9e77804c0a7b45157b6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385439"
---
# <a name="trigger-element-visio-xml"></a>トリガー要素 ' Visio XML (')

Visio ファイル内のドキュメント パーツ間の関係を再計算するための Microsoft Visio に指示を提供します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Trigger_Type](trigger_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml をマスター、# .xml のページ  <br/> |
   
## <a name="definition"></a>定義

```XML
<xs:element name="Trigger" type="Trigger_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |図形の定義に関する情報を提供するセル要素を指定します。  <br/> |
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |DocumentSheet 構造体を定義します。  <br/> |
|[スタイル シート](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheets_type-complextypevisio-xml.md) <br/> |図面で定義されているスタイルを表します。  <br/> |
|[PageSheet (Master_Type の複合型)](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |マスターに関連付けられている図面ページのプロパティを指定します。  <br/> |
|[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |図面ページに関連付けられている図面ページのプロパティを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-trigger_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面の参照をページを指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|N  <br/> |xsd:string  <br/> |必須  <br/> |トリガーがアクティブになったときに呼び出される数式の名前です。  <br/> 「解説」を参照してください。  <br/> |Xsd:string の値を入力します。  <br/> |
   
## <a name="remarks"></a>備考

この**トリガー**の要素の**N**属性は、限られたトリガーの命令に対応する値のいずれかである必要があります。 この**トリガー**の要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**親要素**|**説明**|
|:-----|:-----|:-----|
|されています。  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**HASCATEGORIES**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcBkgPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**BKGPAGENAME**関数を使用してクロス部分の参照が存在する場合は、ページに表示するトリガー  <br/> |
|RecalcColor  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |ページまたはコンテナー内の図形のいずれか、 **RGB**関数を使用するたびに、ページに表示するトリガーです。  <br/> |
|RecalcCreateDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCCREATION**関数を使用してクロス部分の参照が存在する場合、ドキュメントの表示をトリガーします。  <br/> |
|RecalcData1  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA1**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcData2  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA2**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcData3  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**DATA3**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcEditDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTEDIT**関数を使用してクロス部分の参照が存在する場合、ドキュメントの表示をトリガーします。  <br/> |
|RecalcID  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**ID**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcMasterName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**MASTERNAME**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcName  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**名前**の関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcNowAndRand  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |ページまたはコンテナーの図形のいずれかのいずれかの**ようになりました**」または「 **RAND**関数がある場合ページに表示するトリガーです。  <br/> |
|RecalcPageCount  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**PAGECOUNT**関数を使用してクロス部分の参照が存在する場合、ドキュメントの表示をトリガーします。  <br/> |
|RecalcPageName  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> [Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**PAGENAME**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RecalcPageNum  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**PAGENUMBER**関数を使用してクロス部分の参照が存在する場合は、ページに表示するトリガーです。  <br/> |
|RecalcPath  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**POINTALONGPATH**、 **PATHLENGTH**、または**PATHSEGMENT**関数を使用してクロス部分の参照操作を実行するときに、図形に表示するトリガーが存在しています。  <br/> |
|RecalcPrintDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTPRINT**関数を使用してクロス部分の参照が存在する場合、ドキュメントの表示をトリガーします。  <br/> |
|RecalcSaveDT  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**DOCLASTSAVE**関数を使用してクロス部分の参照が存在する場合、ドキュメントの表示をトリガーします。  <br/> |
|RecalcSummary  <br/> |[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |**カテゴリ**、**作成者**、**説明**、**キーワード**、**件名**、または**タイトル**の関数を使用してクロス部分の参照操作を実行すると、ドキュメントに表示されているトリガーが存在しています。  <br/> |
|RecalcType  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**種類**の関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|RelChanged  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**CONTAINERMEMBERCOUNT**関数を使用してクロス部分の参照が存在する場合、図形に表示するトリガーです。  <br/> |
|ZOrderChanged  <br/> |[PageSheet (Page_Type complexType)](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |**CONTAINERSHEETREF**関数を使用してクロス部分の参照が存在する場合は、ページに表示するトリガーです。  <br/> |
|Path  <br/> |[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |**POINTALONGPATH**、 **PATHLENGTH**、または**PATHSEGMENT**関数を使用してクロス部分の参照操作を実行すると、ページに表示されるトリガーが存在しています。  <br/> |
   

