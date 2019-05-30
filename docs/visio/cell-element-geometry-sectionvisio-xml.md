---
title: Cell 要素 (Geometry セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: '[Geometry] セクションを構成する線および円弧に関して、書式設定と動作のプロパティを決定するプロパティを定義します。'
ms.openlocfilehash: 93cc7e204d97a813fea2db4b84c36dedf19cf5f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539808"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Cell 要素 (Geometry セクション) (Visio XML)

[Geometry] セクションを構成する線および円弧に関して、書式設定と動作のプロパティを決定するプロパティを定義します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |マスター # .xml、ページ # .xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで**sequence**、 **minOccurs**、 **maxOccurs**、 **choice**などの特定の要件が定義されている場合は、「定義」セクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Row 要素 (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |[Geometry] セクションを構成する線および円弧に関して、書式設定と動作のプロパティを決定するプロパティを定義します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: string  <br/> |省略可能  <br/> |数式がエラーとして評価されることを示します。 **E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラーメッセージ文字列。  <br/> |
|F  <br/> |xsd: string  <br/> |省略可能  <br/> | 要素の数式を表します。 この属性には、次のいずれかの文字列を含めることができます。  <br/>  ' (一部の数式) ' (数式がローカルに存在する場合)  <br/>  `No Formula`数式がローカルで削除またはブロックされている場合  <br/>  `Inh`数式が継承されている場合。  <br/> |数式。  <br/> |
|N  <br/> |xsd: string  <br/> |必須  <br/> |シェイプシートセルの名前を表します。  <br/> |シェイプシートセルの名前を指定します。  <br/> 下記の「備考」を参照してください。  <br/> |
|U  <br/> |xsd: string  <br/> |省略可能  <br/> |既定値は DL である計量単位を表します。  <br/> |セルの単位を示します。  <br/> |
|V  <br/> |xsd: string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプシートセルの値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。 この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|[Nofill]  <br/> |パスに塗りつぶしを適用するかどうかを指定します。  <br/> |[[NoFill] セル ([Geometry] セクション)](nofill-cell-geometry-section.md) <br/> |
|[Noline]  <br/> |パスの境界に線を描画するかどうかを指定します。  <br/> |[[NoLine] セル ([Geometry] セクション)](noline-cell-geometry-section.md) <br/> |
|[Noquickdrag]  <br/> |ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックしたときに、図形を選択またはドラッグできるかどうかを指定します。  <br/> |[[NoQuickDrag] セル ([Geometry] セクション)](noquickdrag-cell-geometry-section.md) <br/> |
|[Noshow]  <br/> |図面ページにパスを表示するかどうかを示します。  <br/> |[[NoShow] セル ([Geometry] セクション)](noshow-cell-geometry-section.md) <br/> |
|[Nosnap]  <br/> |他の図形がパスにスナップされるかどうかを指定します。  <br/> |[[NoSnap] セル ([Geometry] セクション)](nosnap-cell-geometry-section.md) <br/> |
   

