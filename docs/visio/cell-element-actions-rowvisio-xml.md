---
title: Cell 要素 ([Actions] 行) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: ショートカットメニューまたはアクションタグメニューで、ユーザー設定のコマンドに関連付けられているアクションの1つのプロパティを指定します。
ms.openlocfilehash: 01b81a593de07be8059263d7a6e6538f31ed3be1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356274"
---
# <a name="cell-element-actions-row-visio-xml"></a>Cell 要素 ([Actions] 行) (' Visio XML ')

ショートカットメニューまたはアクションタグメニューで、ユーザー設定のコマンドに関連付けられているアクションの1つのプロパティを指定します。
  
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
|[Row 要素 (Actions セクション)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |ショートカットメニューまたはアクションタグメニューで、ユーザー設定のコマンドに関連付けられているアクションの1つのプロパティを指定します。  <br/> |
   
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
|アクション  <br/> |ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。  <br/> |[[Action] セル ([Actions] セクション)](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |このアクションのメニューに区切り記号を挿入するかどうかを示します。  <br/> |[[BeginGroup] セル ([Actions] セクション)](begingroup-cell-actions-section.md) <br/> |
|buttonface]  <br/> |ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。  <br/> |[[ButtonFace] セル ([Actions] セクション)](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |ショートカット メニューまたはアクション タグ メニューで項目がチェックされているかどうかを示します。  <br/> |[[Checked] セル ([Actions] セクション)](checked-cell-actions-section.md) <br/> |
|無効  <br/> |ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。  <br/> |[[Disabled] セル ([Actions] セクション)](disabled-cell-actions-section.md) <br/> |
|flyoutchild]  <br/> |行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。  <br/> |[flyoutchild] セル (Actions セクション)](flyoutchild-cell-actions-section.md) <br/> |
|可視  <br/> |アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。  <br/> |[[Invisible] セル ([Actions] セクション)](invisible-cell-actions-section.md) <br/> |
|メニュー  <br/> |図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。  <br/> |[[Menu] セル ([Actions] セクション)](menu-cell-actions-section.md) <br/> |
|該当  <br/> |ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。  <br/> |[[ReadOnly] セル ([Actions] セクション)](readonly-cell-actions-section.md) <br/> |
|[sortkey]  <br/> |ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。  <br/> |[[sortkey] セル ([actions] セクション) [sortkey] セル ([actions] セクション)](sortkey-cell-actions-section.md) <br/> |
|[tagname]  <br/> |このアクションに関連付けられているアクション タグの名前を指定します。  <br/> |[[TagName] セル ([Actions] セクション)](tagname-cell-actions-section.md) <br/> |
   

