---
title: セル要素 (ハイパーリンクの行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: 図形に関連付けられた、単一のハイパーリンクの情報を格納します。図形には、各ハイパーリンクに対して 1 つの [Hyperlink] 行があります。
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804961"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>セル要素 (ハイパーリンクの行) ('Visio XML')

図形に関連付けられている 1 つのハイパーリンクの情報が含まれています。 図形には、ハイパーリンクごとに 1 つの**ハイパーリンク**の行が含まれています。 
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[行要素 (ハイパーリンクを参照)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |図形に関連付けられている 1 つのハイパーリンクの情報が含まれています。 図形には、ハイパーリンクごとに 1 つの**ハイパーリンク**の行が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図面ページへの参照を指定します。  <br/> |
   
### <a name="attributes"></a>属性

|**属性**|**型**|**必須**|**説明**|**使用可能な値**|
|:-----|:-----|:-----|:-----|:-----|
|DurationFormat 要素  <br/> |xsd:string  <br/> |省略可能  <br/> |数式がエラーが発生することを示します。 **E**の値は、現在の値 (エラー メッセージの文字列) です。**V**属性の値は、最後の有効な値です。  <br/> |エラー メッセージの文字列です。  <br/> |
|ExternalTaskProject 要素  <br/> |xsd:string  <br/> |省略可能  <br/> | 要素の式を表します。 この属性は、次の文字列のいずれかを含めることができます。  <br/>  '(いくつかの数式)' の数式がローカルに存在する場合  <br/>  `No Formula`数式がローカルで削除されるか、ブロックされている場合  <br/>  `Inh`場合は、数式が継承されます。  <br/> |数式です。  <br/> |
|MultipleCriticalPaths 要素  <br/> |xsd:string  <br/> |必須  <br/> |シェイプ シート セルの名前を表します。  <br/> |シェイプ シート セルの名前です。  <br/> 以下の「解説」セクションを参照してください。  <br/> |
|U  <br/> |xsd:string  <br/> |省略可能  <br/> |既定の測定単位を表しますが、DL です。  <br/> |セルの単位です。  <br/> |
|V  <br/> |xsd:string  <br/> |省略可能  <br/> |セルの値を表します。  <br/> |シェイプ シート セルの値です。  <br/> |
   
## <a name="remarks"></a>備考

この**セル**要素の**N**属性は、限られた一連のシェイプ シートのセルに対応する値のいずれかである必要があります。 この**セル**要素に対して許可されている**N**属性の値を決定するのには次の表を参照してください。 
  
|**値**|**説明**|**詳細については**|
|:-----|:-----|:-----|
|Address  <br/> |移動先の URL アドレス、ファイル名、または UNC パスを指定します。  <br/> |[[Address] セル ([Hyperlinks] セクション)](address-cell-hyperlinks-section.md) <br/> |
|Default  <br/> |図形またはページの既定のハイパーリンクを指定します。  <br/> |[[Default] セル ([Hyperlinks] セクション)](default-cell-hyperlinks-section.md) <br/> |
|説明  <br/> |ハイパーリンクの説明文を表示します。  <br/> |[[Description] セル ([Hyperlinks] セクション)](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |イメージ マップの座標など、URL の解決に使用される情報を渡す文字列を表します。  <br/> |[[ExtraInfo] セル ([Hyperlinks] セクション)](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |コンテナー アプリケーション内で、Visio アプリケーションが ActiveX の文書として開く場合、ターゲットとなるフレームの名前を表します。既定では、空の文字列です。  <br/> |[[Frame] セル ([Hyperlinks] セクション)](frame-cell-hyperlinks-section.md) <br/> |
|非表示  <br/> |図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。  <br/> |[[Invisible] セル ([Hyperlinks] セクション)](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |ハイパーリンクを新しいウィンドウで開くかどうかを指定します。  <br/> |[[NewWindow] セル ([Hyperlinks] セクション)](newwindow-cell-hyperlinks-section.md) <br/> |
|[Sortkey]  <br/> |ショートカット メニューに表示されるハイパーリンクの順序を特定する数です。  <br/> |[[SortKey] セル ([Hyperlinks] セクション)](sortkey-cell-hyperlinks-section.md) <br/> |
|サブアドレス  <br/> |リンク先のターゲット図面内での位置を指定します。  <br/> |[[SubAddress] セル ([Hyperlinks] セクション)](subaddress-cell-hyperlinks-section.md) <br/> |
   

