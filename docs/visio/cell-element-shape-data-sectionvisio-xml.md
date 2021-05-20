---
title: Cell 要素 (Shape Data Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: 図形データのいずれかのプロパティを指定します。
ms.openlocfilehash: 3a6238f19f27d001d3c9eebcbcec720822a0ed40
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539377"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Cell 要素 (Shape Data Section) (Visio XML)

図形データのいずれかのプロパティを指定します。
  
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
|[Row 要素 ([図形データ] セクション)](row-element-shape-data-sectionvisio-xml.md) <br/> |[図形Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |データを図形に関連付けする 1 つの図形データ エントリを指定します。  <br/> |
   
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
|カレンダー  <br/> |図形データ項目の [Type] の値が "日付" のときに、使用するカレンダーの種類を指定します。  <br/> |[[Calendar] セル ([Shape Data] セクション)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |[図形データ] 行が現在、データ レコードセットのフィールドにリンクされているかどうかを示します。  <br/> ||
|Format  <br/> |図形データ項目の書式を指定します。文字列、固定リスト、数値、可変リスト、日付/時刻、期間、または通貨を指定できます。  <br/> |[[Format] セル ([Shape Data] セクション)](format-cell-shape-data-section.md) <br/> |
|非表示  <br/> |[図形データ] ウィンドウに、図形データ項目を表示するかどうかを指定します。  <br/> |[[Invisible] セル ([Shape Data] セクション)](invisible-cell-shape-data-section.md) <br/> |
|ラベル  <br/> |[図形データ] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。  <br/> |[[Label] セル ([Shape Data] セクション)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |図形データ値の記入に使用した言語を示します。  <br/> |[[LangID] セル ([Shape Data] セクション)](langid-cell-shape-data-section.md) <br/> |
|プロンプト  <br/> |[図形データ] ウィンドウで値の上にマウスを置いたときにヒントとして表示される説明または手順を示すテキストを指定します。  <br/> |[[Prompt] セル ([Shape Data] セクション)](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |このセルの値は文字列として扱われ、評価されます。この値に基づいて、[図形データ] ウィンドウ内にある項目を一覧表示するための順序が決まります。  <br/> |[[SortKey] セル ([Shape Data] セクション)](sortkey-cell-shape-data-section.md) <br/> |
|型  <br/> |図形データ値のデータの種類を指定します。  <br/> |[[Type] セル ([Shape Data] セクション)](type-cell-shape-data-section.md) <br/> |
|値  <br/> |[図形データの定義] ダイアログ ボックスに入力した図形データ項目の値が格納されています。  <br/> |[[Value] セル ([Shape Data] セクション)](value-cell-shape-data-section.md) <br/> |
|確認する  <br/> |インスタンスの作成時、または図形の複製またはコピー時に、ユーザーが図形のカスタム プロパティ情報を入力するためにクエリを実行するかどうかを指定します。  <br/> |なし。  <br/> |
   

