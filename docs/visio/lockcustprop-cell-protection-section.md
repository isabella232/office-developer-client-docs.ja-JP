---
title: '[LockCustProp] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
localization_priority: Normal
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: かどうかユーザーを追加、削除、したり、[図形データ] ウィンドウの [図形データの定義] ダイアログ ボックスまたはショート カット メニューを使用してユーザー インターフェイス (UI) 内の図形データの変更を決定します。
ms.openlocfilehash: a88da9e4973f819b398b5bdeda434ede14640797
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805752"
---
# <a name="lockcustprop-cell-protection-section"></a>[LockCustProp] セル ([Protection] セクション)

かどうかユーザーを追加、削除、したり、[**図形データ**] ウィンドウの [**図形データの定義**] ダイアログ ボックスまたはショート カット メニューを使用してユーザー インターフェイス (UI) 内の図形データの変更を決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**のコマンドは無効です。  <br/> |
|FALSE  <br/> |[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**コマンドが有効になっている (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

この値が TRUE の場合でも、図形データ項目の値は変更できます。また、[シェイプシート] ウィンドウの [図形データ] セクションも変更できます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockCustProp] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockCustProp  <br/> |
   
プログラムから、インデックスによって [LockCustProp] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockCustProp** <br/> |
   

