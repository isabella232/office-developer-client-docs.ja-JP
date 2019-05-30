---
title: Cell 要素 (接続行) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: 図形上の1つの接続ポイントの x 座標または y 座標、水平方向または垂直方向、または種類を格納します。
ms.openlocfilehash: 0c8177767d5c85d505ba8a2a430946fd29cf44aa
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541877"
---
# <a name="cell-element-connection-row-visio-xml"></a>Cell 要素 (接続行) (Visio XML)

図形上の1つの接続ポイントの x 座標または y 座標、水平方向または垂直方向、または種類を格納します。
  
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
|[Row 要素 (接続セクション)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |図形上にある単一の接続ポイントに関する、x 座標と y 座標、水平方向と垂直方向、種類を格納します。  <br/> |
   
### <a name="child-elements"></a>子要素

|**Element**|**型**|**説明**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |図形上の1つの接続ポイントに対する x 座標または y 座標、水平方向と垂直方向、および種類を格納します。  <br/> |
   
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
|AutoGen  <br/> |接続ポイントが自動的に生成されるかどうかを指定します。 値が1の場合は、接続ポイントが自動的に生成されることを示します。  <br/> |なし。  <br/> |
|[Dirx  <br/> |対応する接続ポイントに必要な整列ベクトルの x コンポーネントを指定します。  <br/> |[[DirX / A] セル ([Connection Points] セクション)](dirxa-cell-connection-points-section.md) <br/> |
|[Diry  <br/> |対応する接続ポイントに必要な整列ベクトルの y コンポーネントを指定します。  <br/> |[[DirY / B] セル ([Connection Points] セクション)](diryb-cell-connection-points-section.md) <br/> |
|プロンプト  <br/> |この属性は、今後の使用のために予約されています。  <br/> |なし。  <br/> |
|型  <br/> |接続ポイントの種類を指定します。  <br/> |[[Type / C] セル ([Connection Points] セクション)](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |接続ポイントの x 座標をローカル座標で表します。  <br/> |[[X] セル ([Connection Points] セクション)](x-cell-connection-points-section.md) <br/> |
|Y  <br/> |接続ポイントの y 座標をローカル座標で指定します。  <br/> |[[Y] セル ([Connection Points] セクション)](y-cell-connection-points-section.md) <br/> |
   

