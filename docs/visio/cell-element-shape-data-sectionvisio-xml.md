---
title: セル要素 (図形データ セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: 図形データの 1 つのプロパティを指定します。
ms.openlocfilehash: 5e0c79d9439fb3800a277e039143060eec708b11
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390646"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>セル要素 (図形データ セクション)'Visio XML (')

図形データの 1 つのプロパティを指定します。
  
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
|[Row 要素 ([図形データ] セクション)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Data_Type を図形します。](propertyrow_type-complextypevisio-xml.md) <br/> |データを図形に関連付けるための 1 つの図形データの入力を指定します。  <br/> |
   
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
|予定表  <br/> |図形データ項目の [Type] の値が "日付" のときに、使用するカレンダーの種類を指定します。  <br/> |[[Calendar] セル ([Shape Data] セクション)](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |図形データ行がデータ レコード セット内のフィールドに現在リンクされているかどうかを示します。  <br/> ||
|Format  <br/> |図形データ項目の書式を指定します。文字列、固定リスト、数値、可変リスト、日付/時刻、期間、または通貨を指定できます。  <br/> |[[Format] セル ([Shape Data] セクション)](format-cell-shape-data-section.md) <br/> |
|非表示  <br/> |[図形データ] ウィンドウに、図形データ項目を表示するかどうかを指定します。  <br/> |[[Invisible] セル ([Shape Data] セクション)](invisible-cell-shape-data-section.md) <br/> |
|ラベル  <br/> |[図形データ] ウィンドウに表示されるラベルを指定します。ラベルには、英数字とアンダースコア (_) 文字を使用できます。  <br/> |[[Label] セル ([Shape Data] セクション)](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |図形データ値の記入に使用した言語を示します。  <br/> |[[LangID] セル ([Shape Data] セクション)](langid-cell-shape-data-section.md) <br/> |
|プロンプト  <br/> |[図形データ] ウィンドウで値の上にマウスを置いたときにヒントとして表示される説明または手順を示すテキストを指定します。  <br/> |[[Prompt] セル ([Shape Data] セクション)](prompt-cell-shape-data-section.md) <br/> |
|[Sortkey]  <br/> |このセルの値は文字列として扱われ、評価されます。この値に基づいて、[図形データ] ウィンドウ内にある項目を一覧表示するための順序が決まります。  <br/> |[[SortKey] セル ([Shape Data] セクション)](sortkey-cell-shape-data-section.md) <br/> |
|種類  <br/> |図形データ値のデータの種類を指定します。  <br/> |[[Type] セル ([Shape Data] セクション)](type-cell-shape-data-section.md) <br/> |
|値  <br/> |[図形データの定義] ダイアログ ボックスに入力した図形データ項目の値が格納されています。  <br/> |[[Value] セル ([Shape Data] セクション)](value-cell-shape-data-section.md) <br/> |
|確認  <br/> |インスタンスが作成されるか、図形を複製またはコピーしたときに図形のカスタム プロパティ情報を入力するユーザーを照会するかどうかを指定します。  <br/> |なし。  <br/> |
   

