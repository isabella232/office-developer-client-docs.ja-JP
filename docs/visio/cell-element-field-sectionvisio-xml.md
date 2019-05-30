---
title: Cell 要素 (フィールドセクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: '[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。'
ms.openlocfilehash: b3bae89d20a4defed591e95ce0155f70d806e6f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540057"
---
# <a name="cell-element-field-section-visio-xml"></a>Cell 要素 (フィールドセクション) (Visio XML)

[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。
  
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
|[Row 要素 (フィールドセクション)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |[フィールド] ダイアログ ボックスを使用して図形のテキストに挿入した関数および数式を表示します。  <br/> |
   
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
|カレンダー  <br/> |データ型が Date のときに、テキストフィールドに使用するカレンダーを指定します。  <br/> |[[Calendar] セル ([Text Fields] セクション)](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |テキスト フィールドの書式を指定します。文字列、数値、日付/時刻、期間、または通貨を指定できます。  <br/> |[[Format] セル ([Text Fields] セクション)](format-cell-text-fields-section.md) <br/> |
|[Objectkind]  <br/> |テキスト フィールドの種類を示します。  <br/> |[[ObjectKind] セル ([Text Fields] セクション)](objectkind-cell-text-fields-section.md) <br/> |
|型  <br/> |テキスト フィールドの値に対してデータの種類を指定します。  <br/> |[[Type] セル ([Text Fields] セクション)](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |挿入するフィールドの分類を指定します。 このセルは、フィールドおよびカテゴリの情報を決定するために、[フィールドおよびデータの書式] ダイアログボックスで使用されます。  <br/> |[[UICategory] セル ([Text Fields] セクション)](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |挿入するフィールドのコードを指定します。 このセルは、フィールドおよびカテゴリの情報を決定するために、[フィールドおよびデータの書式] ダイアログボックスで使用されます。  <br/> |[[UICode] セル ([Text Fields] セクション)](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |挿入するフィールドの書式を指定します。 このセルは、フィールドおよびデータ形式のダイアログボックスで使用され、フィールドを決定します。  <br/> |[[UIFormat] セル ([Text Fields] セクション)](uiformat-cell-text-fields-section.md) <br/> |
|値  <br/> |フィールドの関数が格納されます。  <br/> |[[Value] セル ([Text Fields] セクション)](value-cell-text-fields-section.md) <br/> |
   

