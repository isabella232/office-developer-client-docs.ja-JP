---
title: Cell 要素 (Controls 行) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: 図形に定義されている特定のコントロールハンドルのプロパティが含まれています。
ms.openlocfilehash: ea54865a645486dfba53688278cb380142899d77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356092"
---
# <a name="cell-element-controls-row-visio-xml"></a>Cell 要素 (Controls 行) (' Visio XML ')

図形に定義されている特定のコントロールハンドルのプロパティが含まれています。
  
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
|[Row 要素 (Controls セクション)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |図形に定義されている特定のコントロールハンドルのプロパティが含まれています。  <br/> |
   
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
   
## <a name="remarks"></a>解説

この**Cell**要素の**N**属性は、シェイプシートのセルに対応する、制限された値のセットのいずれかである必要があります。 この**Cell**要素に対して許可されている**N**属性の値を確認するには、次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|CanGlue  <br/> |コントロール ハンドルを他の図形に接着できるかを指定します。  <br/> |[[Can Glue] セル ([Controls] セクション)](can-glue-cell-controls-section.md) <br/> |
|プロンプト  <br/> |ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを重ねたときに表示されます。  <br/> |[[Tip] セル ([Controls] セクション)](tip-cell-controls-section.md) <br/> |
|X  <br/> |図形のコントロール ハンドルの位置を示す x 座標を、ローカル座標で表します。  <br/> |[[X] セル ([Controls] セクション)](x-cell-controls-section.md) <br/> |
|xCon  <br/> |ハンドルを移動した後に、コントロールハンドルの x 座標が示す動作の種類を指定します。  <br/> |なし。  <br/> |
|xDyn  <br/> |コントロール ハンドルのアンカー ポイントの x 座標を、ローカル座標で表します。  <br/> |[[X Dynamics] セル ([Controls] セクション)](x-dynamics-cell-controls-section.md) <br/> |
|Y  <br/> |図形のコントロール ハンドルの位置を示す y 座標を、ローカル座標で表します。  <br/> |[[Y] セル ([Controls] セクション)](y-cell-controls-section.md) <br/> |
|ycon  <br/> |ハンドルを移動したときにコントロールハンドルの y 座標が表示される動作の種類を指定します。  <br/> |なし。  <br/> |
|YDyn  <br/> |コントロール ハンドルのアンカー ポイントの y 座標を、ローカル座標で表します。  <br/> |[[Y Dynamics] セル ([Controls] セクション)](y-dynamics-cell-controls-section.md) <br/> |
   

