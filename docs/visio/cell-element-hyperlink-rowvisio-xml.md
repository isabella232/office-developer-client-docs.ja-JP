---
title: Cell 要素 (ハイパーリンク行) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: 499a5012afdda1b9cc5149fa9e5aa356e39d11c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623475"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Cell 要素 (ハイパーリンク行) (Visio XML)

図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、ハイパーリンクごとに **1 つのハイパーリンク** 行が含まれる。 
  
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
|[Row 要素 (ハイパーリンク セクション)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、ハイパーリンクごとに **1 つのハイパーリンク** 行が含まれる。  <br/> |
   
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
|Address  <br/> |移動先の URL アドレス、ファイル名、または UNC パスを指定します。  <br/> |[[Address] セル ([Hyperlinks] セクション)](address-cell-hyperlinks-section.md) <br/> |
|既定値  <br/> |図形またはページの既定のハイパーリンクを指定します。  <br/> |[[Default] セル ([Hyperlinks] セクション)](default-cell-hyperlinks-section.md) <br/> |
|説明  <br/> |ハイパーリンクの説明文を表示します。  <br/> |[[Description] セル ([Hyperlinks] セクション)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。  <br/> |[[ExtraInfo] セル ([Hyperlinks] セクション)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。  <br/> |[[Frame] セル ([Hyperlinks] セクション)](frame-cell-hyperlinks-section.md) <br/> |
|非表示  <br/> |図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。  <br/> |[[Invisible] セル ([Hyperlinks] セクション)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。  <br/> |[[NewWindow] セル ([Hyperlinks] セクション)](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。  <br/> |[[SortKey] セル ([Hyperlinks] セクション)](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |リンク先のターゲット図面内での位置を指定します。  <br/> |[[SubAddress] セル ([Hyperlinks] セクション)](subaddress-cell-hyperlinks-section.md) <br/> |
   

