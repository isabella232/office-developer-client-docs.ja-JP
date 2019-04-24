---
title: '[Actions] 行 ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
localization_priority: Normal
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: ショートカットメニューまたはアクションタグメニューで、ユーザー設定のコマンドに関連付けられているアクションを指定するセルが含まれています。 [Actions] セクションには、各アクションごとに 1 つの [Actions] 行があります。
ms.openlocfilehash: 37464e98b3e4f7d07b2ae4bd391b31ec009b6726
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283045"
---
# <a name="actions-row-actions-section"></a>[Actions] 行 ([Actions] セクション)

ショートカットメニューまたはアクションタグメニューで、ユーザー設定のコマンドに関連付けられているアクションを指定するセルが含まれています。 [Actions] セクションには、各アクションごとに 1 つの [Actions] 行があります。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
[Actions] 行の名前は Actions. 次のセルに*名前*とが含まれます。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |ショートカット メニューまたはアクション タグ メニューの項目を選択したときに実行される数式が格納されています。  <br/> |
|[メニュー](menu-cell-actions-section.md) <br/> |アクションタグまたはショートカットメニューに表示されるメニュー項目の名前を定義します。  <br/> |
|[[tagname]](tagname-cell-actions-section.md) <br/> |このアクションを表示するアクション タグの論理名を指定します。  <br/> |
|[buttonface]](buttonface-cell-actions-section.md) <br/> |ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。  <br/> |
|[[sortkey]](sortkey-cell-actions-section.md) <br/> |アクション タグ メニューまたはショートカット メニューに表示されるメニュー項目の順序を指定するための数字です。  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |アクションタグまたはショートカットメニューでメニュー項目がチェックされているかどうかを示します。  <br/> |
|[Disabled](disabled-cell-actions-section.md) <br/> |ショートカット メニューまたはアクション タグ メニューのメニュー項目が無効かどうかを示します。  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |メニュー項目が読み取り専用 (クリックできない) かどうかを示します。  <br/> |
|[可視](invisible-cell-actions-section.md) <br/> |アクション タグ メニューまたはショートカット メニューにメニュー項目が表示されるかどうかを示します。  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |メニュー項目の上に区切り記号を挿入するかどうかを指定します。  <br/> |
   
## <a name="remarks"></a>解説

 必要に応じて [Actions.  必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。 既存の [Actions] セクションにカスタム コマンドを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルを行名で参照できます。これは、シェイプシートウィンドウに赤いテキストで表示されます。 アクションにわかりやすい名前を割り当てる。 [*名前*] 行をクリックし、[ *custom* ] などの名前を入力して、行名のアクションを作成します (例: custom)。 その後、[Actions] を使用して [menu] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

