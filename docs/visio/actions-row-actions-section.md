---
title: '[Actions] 行 ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60017
ms.localizationpriority: medium
ms.assetid: 29a7464a-b9d4-a8ea-161b-3044de32ed23
description: ショートカットまたはアクション タグ メニューのカスタム コマンドに関連付けられたアクションを指定するセルを含む。 [Actions] セクションには、各アクションごとに 1 つの [Actions] 行があります。
ms.openlocfilehash: 21b0fe801b7041f7de9a7b4dfcd559e8ea553356
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616132"
---
# <a name="actions-row-actions-section"></a>[Actions] 行 ([Actions] セクション)

ショートカットまたはアクション タグ メニューのカスタム コマンドに関連付けられたアクションを指定するセルを含む。 [Actions] セクションには、各アクションごとに 1 つの [Actions] 行があります。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
[Actions] 行の名前は Actions. *名前*  を指定し、次のセルを含む。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[Action](action-cell-actions-section.md) <br/> |ショートカット メニューまたはアクション タグ メニューの項目を選択したときに実行される数式が格納されています。  <br/> |
|[メニュー](menu-cell-actions-section.md) <br/> |アクション タグまたはショートカット メニューに表示されるメニュー項目の名前を定義します。  <br/> |
|[TagName](tagname-cell-actions-section.md) <br/> |このアクションを表示するアクション タグの論理名を指定します。  <br/> |
|[ButtonFace](buttonface-cell-actions-section.md) <br/> |ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。  <br/> |
|[SortKey](sortkey-cell-actions-section.md) <br/> |アクション タグ メニューまたはショートカット メニューに表示されるメニュー項目の順序を指定するための数字です。  <br/> |
|[Checked](checked-cell-actions-section.md) <br/> |アクション タグまたはショートカット メニューでメニュー項目をオンにするかどうかを示します。  <br/> |
|[Disabled](disabled-cell-actions-section.md) <br/> |ショートカット メニューまたはアクション タグ メニューのメニュー項目が無効かどうかを示します。  <br/> |
|[ReadOnly](readonly-cell-actions-section.md) <br/> |メニュー項目が読み取り専用 (クリックできない) かどうかを示します。  <br/> |
|[非表示](invisible-cell-actions-section.md) <br/> |アクション タグ メニューまたはショートカット メニューにメニュー項目が表示されるかどうかを示します。  <br/> |
|[BeginGroup](begingroup-cell-actions-section.md) <br/> |メニュー項目の上にある区切り記号をメニューに挿入するかどうかを示します。  <br/> |
   
## <a name="remarks"></a>注釈

 必要に応じて [Actions.  *必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。 既存の [Actions] セクションにカスタム コマンドを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルは行名で参照できます。これは、赤いテキストの ShapeSheet ウィンドウに表示されます。 アクションにわかりやすい名前を割り当てる。 *name* 行をクリックし、カスタムなどの名前を入力して、Actions.Custom という行名を作成します。  次に、Actions.Custom.Menu を使用して [メニュー] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

