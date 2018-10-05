---
title: セル要素 (接続行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: X 座標または y 座標、水平方向または垂直方向、または図形の 1 つの接続ポイントの型が含まれています。
ms.openlocfilehash: 367d7e462c1eb5b8fa6ee0572346f45ad621fa15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388960"
---
# <a name="cell-element-connection-row-visio-xml"></a>セル要素 (接続行) ('Visio XML')

X 座標または y 座標、水平方向または垂直方向、または図形の 1 つの接続ポイントの型が含まれています。
  
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
|[Row 要素 ([接続] セクション)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |X 座標と y 座標、水平方向と垂直方向、および図形上の 1 つの接続ポイントの型が含まれています。  <br/> |
   
### <a name="child-elements"></a>子要素

|**要素**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |X 座標または y 座標、水平方向と垂直方向、および図形上の 1 つの接続ポイントの型が含まれています。  <br/> |
   
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
|自動  <br/> |接続ポイントが自動的に生成されるかどうかを指定します。 1 の値は、コネクション ポイントが自動的に生成されることを示します。  <br/> |なし。  <br/> |
|DirX  <br/> |対応する接続ポイントの必要な整列ベクトルの x コンポーネントを決定します。  <br/> |[[DirX / A] セル ([Connection Points] セクション)](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |対応する接続ポイントの必要な整列ベクトルの y コンポーネントを決定します。  <br/> |[[DirY / B] セル ([Connection Points] セクション)](diryb-cell-connection-points-section.md) <br/> |
|プロンプト  <br/> |この属性は、将来使用するために予約されています。  <br/> |なし。  <br/> |
|種類  <br/> |接続ポイントの種類を指定します。  <br/> |[[Type / C] セル ([Connection Points] セクション)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |接続ポイントの x 座標をローカル座標で表します。  <br/> |[[X] セル ([Connection Points] セクション)](x-cell-connection-points-section.md) <br/> |
|Y  <br/> |ローカル座標での接続ポイントの y 座標を指定します。  <br/> |[[Y] セル ([Connection Points] セクション)](y-cell-connection-points-section.md) <br/> |
   

