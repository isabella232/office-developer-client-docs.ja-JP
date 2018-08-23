---
title: セル要素 (アクション行) ('Visio XML')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: カスタム メニューのコマンドをショートカット メニューまたは操作タグに関連付けられているアクションの 1 つのプロパティを指定します。
ms.openlocfilehash: d0f103e6f241a7982bcc2663752d9338cf4c3eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804932"
---
# <a name="cell-element-actions-row-visio-xml"></a>セル要素 (アクション行) ('Visio XML')

カスタム メニューのコマンドをショートカット メニューまたは操作タグに関連付けられているアクションの 1 つのプロパティを指定します。
  
## <a name="element-information"></a>要素情報

|||
|:-----|:-----|
|**要素の種類** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
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
|[Row 要素 ([操作] セクション)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |カスタム メニューのコマンドをショートカット メニューまたは操作タグに関連付けられているアクションの 1 つのプロパティを指定します。  <br/> |
   
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
|アクション  <br/> |ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。  <br/> |[[Action] セル ([Actions] セクション)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |このアクションのメニューに区切り記号を挿入するかどうかを示します。  <br/> |[[BeginGroup] セル ([Actions] セクション)](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。  <br/> |[[ButtonFace] セル ([Actions] セクション)](buttonface-cell-actions-section.md) <br/> |
|オン  <br/> |ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。  <br/> |[[Checked] セル ([Actions] セクション)](checked-cell-actions-section.md) <br/> |
|Disabled  <br/> |ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。  <br/> |[[Disabled] セル ([Actions] セクション)](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。  <br/> |[[FlyoutChild] セル ([操作] セクション)](flyoutchild-cell-actions-section.md) <br/> |
|非表示  <br/> |アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。  <br/> |[[Invisible] セル ([Actions] セクション)](invisible-cell-actions-section.md) <br/> |
|Menu  <br/> |図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。  <br/> |[[Menu] セル ([Actions] セクション)](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。  <br/> |[[ReadOnly] セル ([Actions] セクション)](readonly-cell-actions-section.md) <br/> |
|[Sortkey]  <br/> |ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。  <br/> |[[Sortkey] セル ([Actions] セクション) [sortkey] セル ([Actions] セクション)](sortkey-cell-actions-section.md) <br/> |
|[Tagname]  <br/> |このアクションに関連付けられているアクション タグの名前を指定します。  <br/> |[[TagName] セル ([Actions] セクション)](tagname-cell-actions-section.md) <br/> |
   

