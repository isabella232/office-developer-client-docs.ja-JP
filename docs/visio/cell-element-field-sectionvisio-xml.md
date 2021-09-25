---
title: Cell 要素 (Field Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: '[フィールド] ダイアログ ボックスを使用して、図形のテキストに挿入された関数と数式を表示します。'
ms.openlocfilehash: fffa97458b083edc7df33c4a559fa987f2bb1bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594896"
---
# <a name="cell-element-field-section-visio-xml"></a>Cell 要素 (Field Section) (Visio XML)

[フィールド] ダイアログ ボックスを使用して、図形のテキストに挿入された関数と数式を表示します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Row 要素 (Field Section)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |[フィールド] ダイアログ ボックスを使用して、図形のテキストに挿入された関数と数式を表示します。  <br/> |
   
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
|予定表  <br/> |データ型が Date の場合にテキスト フィールドに使用されるカレンダーを指定します。  <br/> |[[Calendar] セル ([Text Fields] セクション)](calendar-cell-text-fields-section.md) <br/> |
|フォーマット  <br/> |テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。  <br/> |[[Format] セル ([Text Fields] セクション)](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |テキスト フィールドの種類を示します。  <br/> |[[ObjectKind] セル ([Text Fields] セクション)](objectkind-cell-text-fields-section.md) <br/> |
|種類  <br/> |テキスト フィールドの値に対してデータの種類を指定します。  <br/> |[[Type] セル ([Text Fields] セクション)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |挿入されたフィールドのカテゴリを決定します。 このセルは、[フィールド] ダイアログ ボックスと [データ形式] ダイアログ ボックスで、フィールドおよびカテゴリ情報を決定するために使用されます。  <br/> |[[UICategory] セル ([Text Fields] セクション)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |挿入されたフィールドのコードを決定します。 このセルは、[フィールド] ダイアログ ボックスと [データ形式] ダイアログ ボックスで、フィールドおよびカテゴリ情報を決定するために使用されます。  <br/> |[[UICode] セル ([Text Fields] セクション)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |挿入されたフィールドの形式を指定します。 このセルは、[フィールド] ダイアログ ボックスと [データ形式] ダイアログ ボックスで使用され、フィールドと  <br/> |[[UIFormat] セル ([Text Fields] セクション)](uiformat-cell-text-fields-section.md) <br/> |
|値  <br/> |フィールドの関数が格納されます。  <br/> |[[Value] セル ([Text Fields] セクション)](value-cell-text-fields-section.md) <br/> |
   

