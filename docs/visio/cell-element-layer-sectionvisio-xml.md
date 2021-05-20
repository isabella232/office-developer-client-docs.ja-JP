---
title: Cell 要素 (Layer Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: レイヤーまたはページのプロパティのいずれか 1 つを指定します。
ms.openlocfilehash: 119c82f84c76f735a5d9b73b4bea8beda0a7e476
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539758"
---
# <a name="cell-element-layer-section-visio-xml"></a>Cell 要素 (Layer Section) (Visio XML)

レイヤーまたはページのプロパティのいずれか 1 つを指定します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |masters.xml、pages.xml  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマで **sequence**、**minOccurs**、**maxOccurs**、**choice** などの具体的な要件が定義されている場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Row 要素 (Layer Section)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |レイヤーまたはページのプロパティのいずれか 1 つを指定します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーと評価されるかどうかを示します。 E の値 **は** 、現在の値 (エラー メッセージ文字列) です。V 属性の値 **は** 最後の有効な値です。  <br/> |エラー メッセージ文字列。  <br/> |
|F  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の数式を表します。 この属性には、次のいずれかの文字列を含めできます。  <br/>  式がローカルに存在する場合は'(一部の数式)'  <br/>  `No Formula` 数式がローカルで削除またはブロックされている場合  <br/>  `Inh` 数式が継承されている場合。  <br/> |数式。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |[シェイプシート] セルの名前を表します。  <br/> |[シェイプシート] セルの名前を指定します。  <br/> 以下の「備考」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |測定単位を表します 既定は DL です。  <br/> |セルの単位。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |[シェイプシート] セルの値を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

この **Cell** 要素の N 属性は **、ShapeSheet** セルに対応する制限された値のセットの 1 つである必要があります。 次の表を参照して、この Cell 要素で許可される **N** 属性の値を **決定** します。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|有効  <br/> |レイヤーがアクティブかどうかを指定します。  <br/> |なし。  <br/> |
|色  <br/> |次のいずれかを指定します。レイヤーの表示に使用する色テーブルの色のインデックス、または色テーブルではなくカスタム色を指定する RGB 値を指定します。  <br/> |なし。  <br/> |
|ColorTrans  <br/> |0 (完全に不透明) から 1 (完全に透明) まで、レイヤーまたは図形のテキストの色の透明度を決定します。  <br/> |なし。  <br/> |
|Glue  <br/> |レイヤーに属する図形を接着できるかどうかを指定します。  <br/> |なし。  <br/> |
|Lock  <br/> |レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。  <br/> |なし。  <br/> |
|名前  <br/> |レイヤーの名前。  <br/> |なし。  <br/> |
|NameUniv  <br/> |レイヤーの汎用名を指定します。  <br/> |なし。  <br/> |
|印刷  <br/> |図面の印刷時に、レイヤーに属する図形を印刷するかどうかを指定します。  <br/> |なし。  <br/> |
|スナップ  <br/> |他の図形をレイヤーに割り当てられた図形にスナップできるかどうかを指定します。  <br/> |なし。  <br/> |
|状態  <br/> |レイヤーがドキュメントの有効なレイヤーであるかどうかを指定します。  <br/> |なし。  <br/> |
|Visible  <br/> |レイヤーに属している図形が図面ページに表示されるかどうかを指定します。  <br/> |なし。  <br/> |
   

