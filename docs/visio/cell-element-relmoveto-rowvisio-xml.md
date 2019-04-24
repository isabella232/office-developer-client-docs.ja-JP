---
title: Cell 要素 ([relmoveto] 行) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8e91497c-0aa1-2021-9317-cf989e5b84a3
description: 図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。
ms.openlocfilehash: cc81ea1b36541fe471807e83057e7aaaacb70d70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339572"
---
# <a name="cell-element-relmoveto-row-visio-xml"></a>Cell 要素 ([relmoveto] 行) (' Visio XML ')

図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Row 要素 (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelMoveTo_Type](relmoveto_type-complextypevisio-xml.md) <br/> |図形の最初の頂点に対する x 座標または y 座標、またはパスを切断した後の最初の頂点の x 座標または y 座標を格納します。この値は、図形の高さと幅を基準にしています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd: string  <br/> |省略可能  <br/> |数式がエラーとして評価されることを示します。 **E**の値は、現在の値 (エラーメッセージ文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラーメッセージ文字列。  <br/> |
|F  <br/> |xsd: string  <br/> |省略可能  <br/> | 要素の数式を表します。 この属性には、次のいずれかの文字列を含めることができます。  <br/>  ' (一部の数式) ' (数式がローカルに存在する場合)  <br/>  `No Formula`数式がローカルで削除またはブロックされている場合  <br/>  `Inh`数式が継承されている場合。  <br/> |数式。  <br/> |
|N  <br/> |xsd: string  <br/> |必須  <br/> |シェイプシートセルの名前を表します。  <br/> |シェイプシートセルの名前を指定します。  <br/> 下記の「備考」を参照してください。  <br/> |
|U  <br/> |xsd: string  <br/> |省略可能  <br/> |既定値は DL である計量単位を表します。  <br/> |セルの単位を示します。  <br/> |
|V  <br/> |xsd: string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプシートセルの値を指定します。  <br/> |
   
## <a name="remarks"></a>解説

この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。 この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|X  <br/> |[ **relmoveto** ] 行がセクションの最初の行の場合、[ **x** ] セルは図形の幅を基準にして、図形の最初の頂点に対する x 座標を表します。 2つの行の間に [ **relmoveto** ] 行が表示されている場合、[ **x** ] セルは、パスを切断した後の最初の頂点に対する x 座標を表します。  <br/> |[「relmoveto」行 (「Geometry」セクション)](relmoveto-row-geometry-section.md) <br/> |
|Y  <br/> |[ **relmoveto** ] 行がセクションの最初の行の場合、[ **y** ] セルは、図形の高さを基準にして、図形の最初の頂点に対する y 座標を表します。 2つの行の間に [ **relmoveto** ] 行が表示されている場合、[ **y** ] セルは、パスを切断した後の最初の頂点に対する y 座標を表します。  <br/> |[「relmoveto」行 (「Geometry」セクション)](relmoveto-row-geometry-section.md) <br/> |
   

