---
title: セル要素 (レイヤー ・ セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: レイヤーの 1 つのプロパティ ページのプロパティを指定します。
ms.openlocfilehash: 92be29321ba637bb694c0cf5d3cddcb888618c1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804990"
---
# <a name="cell-element-layer-section-visio-xml"></a>セル要素 (レイヤー ・ セクション)'Visio XML (')

レイヤーの 1 つのプロパティ ページのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |masters.xml、pages.xml  <br/> |
   
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
|[Row 要素 ([レイヤー] セクション)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |レイヤーの 1 つのプロパティ ページのプロパティを指定します。  <br/> |
   
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
   
## <a name="remarks"></a>注釈

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細情報**|
|:-----|:-----|:-----|
|アクティブ  <br/> |レイヤーがアクティブかどうかを指定します。  <br/> |なし。  <br/> |
|色  <br/> |次のいずれかを指定します。 レイヤーまたはカラー テーブルにない独自の色を指定する RGB 値を表示するカラー テーブルで色のインデックスを使用します。  <br/> |なし。  <br/> |
|ColorTrans  <br/> |レイヤーまたは 0 (完全に不透明) から 1 (完全に透明) から、図形のテキストの色の透明度を決定します。  <br/> |なし。  <br/> |
|接着  <br/> |レイヤーに属している図形に接着できるかどうかを指定します。  <br/> |なし。  <br/> |
|Lock  <br/> |レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。  <br/> |なし。  <br/> |
|名前  <br/> |レイヤーの名前。  <br/> |なし。  <br/> |
|NameUniv  <br/> |レイヤーの汎用名を指定します。  <br/> |なし。  <br/> |
|印刷  <br/> |図面を印刷するときに、レイヤーに属している図形が印刷されるかどうかを指定します。  <br/> |なし。  <br/> |
|スナップ  <br/> |レイヤーに割り当てられている図形に他の図形をスナップできるかどうかを指定します。  <br/> |なし。  <br/> |
|Status  <br/> |レイヤーがドキュメントの有効なレイヤーであるかどうかを指定します。  <br/> |なし。  <br/> |
|Visible  <br/> |レイヤーに属している図形が図面ページに表示されるかどうかを指定します。  <br/> |なし。  <br/> |
   

