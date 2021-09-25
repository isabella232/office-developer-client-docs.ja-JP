---
title: Cell 要素 (Action Tag セクション) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: 図形またはページ上のアクション タグに 1 つのプロパティを定義します。
ms.openlocfilehash: ca7c75f364209b2f40d17b4830128d729d762c34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615999"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Cell 要素 (Action Tag セクション) (Visio XML)

図形またはページ上のアクション タグに 1 つのプロパティを定義します。
  
## <a name="element-information"></a>要素の情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**ドキュメント パーツ** <br/> |masters.xml、master#.xml、pages.xml、page#.xml  <br/> |
   
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
|[Row 要素 (ActionTag セクション)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |図形またはページのアクション タグを定義します。  <br/> |
   
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
|ButtonFace  <br/> |アクション タグ ボタンに表示されるボタン イメージの ID を示します。  <br/> |[[ButtonFace] セル ([Action Tags] セクション)](buttonface-cell-action-tags-section.md) <br/> |
|説明  <br/> |アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。  <br/> |[[Description] セル ([Action Tags] セクション)](description-cell-action-tags-section.md) <br/> |
|無効  <br/> |図面ウィンドウに、アクション タグを表示するかどうかを示します。  <br/> |[[Disabled] セル ([Action Tags] セクション)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |ユーザーがポインターをタグの上に移動した場合、図形が選択されている場合、またはすべての時刻にアクション タグが表示されるかどうかを指定します。  <br/> |[[DisplayMode] セル ([Smart Tags] セクション)](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。  <br/> |[[TagName] セル ([Action Tags] セクション)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |図形内で、アクション タグ ボタンが配置されるローカルの x 座標の位置です。  <br/> |[[X] セル ([Action Tags] セクション)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |[X] セルと [Y] セルによって定義された点に対する、アクション タグ ボタンの x 座標のオフセット値です。  <br/> |[[X Justify] セル ([Action Tags] セクション)](x-justify-cell-action-tags-section.md) <br/> |
|Y  <br/> |図形内で、アクション タグ ボタンが配置されるローカルの y 座標の位置です。  <br/> |[[Y] セル ([Action Tags] セクション)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |[X] セルと [Y] セルによって定義された点に対する、アクション タグ ボタンの y 座標のオフセット値です。  <br/> |[[Y Justify] セル ([Action Tags] セクション)](y-justify-cell-action-tags-section.md) <br/> |
   

