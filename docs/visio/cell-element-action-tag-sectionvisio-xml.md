---
title: セル要素 (アクション タグ セクション)'Visio XML (')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: 図形またはページのアクション タグの 1 つのプロパティを定義します。
ms.openlocfilehash: 0945235c49e77210564e50e5c111579ab37f3e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804936"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>セル要素 (アクション タグ セクション)'Visio XML (')

図形またはページのアクション タグの 1 つのプロパティを定義します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の型** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**名前空間** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**スキーマ ファイル** <br/> |VisioSchema15.xsd  <br/> |
|**文書パーツ** <br/> |ページ # .xml、masters.xml、マスターの # .xml、pages.xml  <br/> |
   
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
|[行要素 ([ActionTag] セクション)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |図形またはページ上には、アクション タグを定義します。  <br/> |
   
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
|ButtonFace  <br/> |アクション タグ ボタンに表示されるボタン イメージの ID を示します。  <br/> |[[ButtonFace] セル ([Action Tags] セクション)](buttonface-cell-action-tags-section.md) <br/> |
|説明  <br/> |アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。  <br/> |[[Description] セル ([Action Tags] セクション)](description-cell-action-tags-section.md) <br/> |
|無効  <br/> |図面ウィンドウに、アクション タグを表示するかどうかを示します。  <br/> |[[Disabled] セル ([Action Tags] セクション)](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |アクションのタグには、ユーザーがタグの上、ポインターを移動すると、図形が選択されている場合、またはすべての時間が表示されるかどうかを決定します。  <br/> |[[DisplayMode] セル ([Smart Tags] セクション)](displaymode-cell-action-tags-section.md) <br/> |
|[Tagname]  <br/> |アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。  <br/> |[[TagName] セル ([Action Tags] セクション)](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |図形のローカル座標で中心となるアクション タグ ボタンの x 座標の位置に配置されます。  <br/> |[[X] セル ([Action Tags] セクション)](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |X と Y セルによって定義された点を基準にして、操作タグ ボタンの x オフセット。  <br/> |[[X Justify] セル ([Action Tags] セクション)](x-justify-cell-action-tags-section.md) <br/> |
|Y  <br/> |図形のローカル座標で中心となるアクション タグ ボタンの y 座標の位置に配置されます。  <br/> |[[Y] セル ([Action Tags] セクション)](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |X と Y セルによって定義された点を基準にして、操作タグ ボタンの y オフセット。  <br/> |[[Y Justify] セル ([Action Tags] セクション)](y-justify-cell-action-tags-section.md) <br/> |
   

