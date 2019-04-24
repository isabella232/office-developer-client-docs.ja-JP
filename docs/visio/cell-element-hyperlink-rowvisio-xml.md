---
title: Cell 要素 (ハイパーリンク行) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: 6644dc70f3d3616e5c20587db4eabaaf773c31d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356064"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Cell 要素 (ハイパーリンク行) (' Visio XML ')

図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、ハイパーリンクごとに1つの**ハイパーリンク**行が含まれます。 
  
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
|[Row 要素 (ハイパーリンクセクション)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |図形に関連付けられた、単一のハイパーリンクの情報を格納します。 図形には、ハイパーリンクごとに1つの**ハイパーリンク**行が含まれます。  <br/> |
   
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
|Address  <br/> |移動先の URL アドレス、ファイル名、または UNC パスを指定します。  <br/> |[[Address] セル ([Hyperlinks] セクション)](address-cell-hyperlinks-section.md) <br/> |
|既定値  <br/> |図形またはページの既定のハイパーリンクを指定します。  <br/> |[[Default] セル ([Hyperlinks] セクション)](default-cell-hyperlinks-section.md) <br/> |
|説明  <br/> |ハイパーリンクの説明文を表示します。  <br/> |[[Description] セル ([Hyperlinks] セクション)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。  <br/> |[[ExtraInfo] セル ([Hyperlinks] セクション)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。  <br/> |[[Frame] セル ([Hyperlinks] セクション)](frame-cell-hyperlinks-section.md) <br/> |
|可視  <br/> |図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。  <br/> |[[Invisible] セル ([Hyperlinks] セクション)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。  <br/> |[[NewWindow] セル ([Hyperlinks] セクション)](newwindow-cell-hyperlinks-section.md) <br/> |
|[sortkey]  <br/> |ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。  <br/> |[[SortKey] セル ([Hyperlinks] セクション)](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |リンク先のターゲット図面内での位置を指定します。  <br/> |[[SubAddress] セル ([Hyperlinks] セクション)](subaddress-cell-hyperlinks-section.md) <br/> |
   

