---
title: Cell 要素 ([操作タグ] セクション) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: 図形またはページ上のアクションタグに1つのプロパティを定義します。
ms.openlocfilehash: 61fad8575532adde0106ef6db2888fe38f3ae4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337178"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Cell 要素 ([操作タグ] セクション) (' Visio XML ')

図形またはページ上のアクションタグに1つのプロパティを定義します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15  <br/> |
|**文書パーツ** <br/> |masters、master # .xml、pages .xml、page # .xml  <br/> |
   
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
|[Row 要素 (actiontag セクション)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |図形またはページ上のアクションタグを定義します。  <br/> |
   
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
|buttonface]  <br/> |アクション タグ ボタンに表示されるボタン イメージの ID を示します。  <br/> |[[ButtonFace] セル ([Action Tags] セクション)](buttonface-cell-action-tags-section.md) <br/> |
|説明  <br/> |アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。  <br/> |[[Description] セル ([Action Tags] セクション)](description-cell-action-tags-section.md) <br/> |
|無効  <br/> |図面ウィンドウに、アクション タグを表示するかどうかを示します。  <br/> |[[Disabled] セル ([Action Tags] セクション)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |ユーザーがタグの上にポインターを移動したとき、図形を選択したとき、または常に [アクション] タグを表示するかどうかを指定します。  <br/> |[[DisplayMode] セル ([Smart Tags] セクション)](displaymode-cell-action-tags-section.md) <br/> |
|[tagname]  <br/> |アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。  <br/> |[[TagName] セル ([Action Tags] セクション)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |図形内で、アクション タグ ボタンが配置されるローカルの x 座標の位置です。  <br/> |[[X] セル ([Action Tags] セクション)](x-cell-action-tags-section.md) <br/> |
|xjustify  <br/> |[X] セルと [Y] セルによって定義された点に対する、アクション タグ ボタンの x 座標のオフセット値です。  <br/> |[[X Justify] セル ([Action Tags] セクション)](x-justify-cell-action-tags-section.md) <br/> |
|Y  <br/> |図形内で、アクション タグ ボタンが配置されるローカルの y 座標の位置です。  <br/> |[[Y] セル ([Action Tags] セクション)](y-cell-action-tags-section.md) <br/> |
|yjustify  <br/> |[X] セルと [Y] セルによって定義された点に対する、アクション タグ ボタンの y 座標のオフセット値です。  <br/> |[[Y Justify] セル ([Action Tags] セクション)](y-justify-cell-action-tags-section.md) <br/> |
   

