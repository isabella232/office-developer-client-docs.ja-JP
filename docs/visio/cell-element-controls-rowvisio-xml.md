---
title: セル要素 ([Controls] 行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: 図形に対して定義されている特定のコントロール ハンドルのプロパティが含まれています。
ms.openlocfilehash: ea54865a645486dfba53688278cb380142899d77
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401273"
---
# <a name="cell-element-controls-row-visio-xml"></a>セル要素 ([Controls] 行) ('Visio XML')

図形に対して定義されている特定のコントロール ハンドルのプロパティが含まれています。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |# .xml をマスター、# .xml のページ  <br/> |
   
## <a name="definition"></a>定義

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>要素と属性

スキーマは、**シーケンス**、 **minOccurs**、 **maxOccurs**では、**選択**などの特定の要件を定義する場合は、定義のセクションを参照してください。 
  
### <a name="parent-elements"></a>親要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[Row 要素 ([コントロール] セクション)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |図形に対して定義されている特定のコントロール ハンドルのプロパティが含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーが発生することを示します。 **E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラー メッセージの文字列です。  <br/> |
|ExternalTaskProject 要素  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の式を表します。 この属性は、次の文字列のいずれかを含めることができます。  <br/>  '(いくつかの数式)' の数式がローカルに存在する場合  <br/>  `No Formula`数式がローカルで削除されるか、ブロックされている場合  <br/>  `Inh`場合は、数式が継承されます。  <br/> |数式です。  <br/> |
|N  <br/> |xsd:string  <br/> |必須  <br/> |シェイプ シート セルの名前を表します。  <br/> |シェイプ シート セルの名前です。  <br/> 以下の「解説」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |既定の測定単位を表しますが、DL です。  <br/> |セルの単位です。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプ シート セルの値です。  <br/> |
   
## <a name="remarks"></a>備考

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|CanGlue  <br/> |コントロール ハンドルを他の図形に接着できるかを指定します。  <br/> |[[Can Glue] セル ([Controls] セクション)](can-glue-cell-controls-section.md) <br/> |
|プロンプト  <br/> |ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを重ねたときに表示されます。  <br/> |[[Tip] セル ([Controls] セクション)](tip-cell-controls-section.md) <br/> |
|X  <br/> |図形のコントロール ハンドルの位置を示す x 座標を、ローカル座標で表します。  <br/> |[[X] セル ([Controls] セクション)](x-cell-controls-section.md) <br/> |
|[xcon]  <br/> |コントロール ハンドルの x 座標がハンドルを移動した後に発生する動作の種類を指定します。  <br/> |なし。  <br/> |
|xDyn  <br/> |コントロール ハンドルのアンカー ポイントの x 座標を、ローカル座標で表します。  <br/> |[[X Dynamics] セル ([Controls] セクション)](x-dynamics-cell-controls-section.md) <br/> |
|Y  <br/> |図形のコントロール ハンドルの位置を示す y 座標を、ローカル座標で表します。  <br/> |[[Y] セル ([Controls] セクション)](y-cell-controls-section.md) <br/> |
|YCon  <br/> |ハンドルを移動した後、コントロール ハンドルの y 座標が示す動作の種類を指定します。  <br/> |なし。  <br/> |
|YDyn  <br/> |コントロール ハンドルのアンカー ポイントの y 座標を、ローカル座標で表します。  <br/> |[[Y Dynamics] セル ([Controls] セクション)](y-dynamics-cell-controls-section.md) <br/> |
   

