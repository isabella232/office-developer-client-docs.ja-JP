---
title: '[LockCustProp] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60055
ms.localizationpriority: medium
ms.assetid: d1c23f1d-485d-a897-594d-15d6e8d0fb3c
description: '[図形データの定義] ダイアログ ボックス、または [図形データ] ウィンドウのショートカット メニューを使用して、ユーザー インターフェイス (UI) の図形データを追加、削除、または修正できるかどうかを判別します。'
ms.openlocfilehash: bf8730523b007f8d7e0f4b936d94c8779d160a63
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603635"
---
# <a name="lockcustprop-cell-protection-section"></a>[LockCustProp] セル ([Protection] セクション)

[**図形データの定義**] ダイアログ ボックス、または [**図形データ**] ウィンドウのショートカット メニューを使用して、ユーザー インターフェイス (UI) の図形データを追加、削除、または修正できるかどうかを判別します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**] コマンドが無効になります。  <br/> |
|FALSE  <br/> |[**図形データ**] ウィンドウのショートカット メニューの [**図形データの定義**] コマンドが有効になります (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

この値が TRUE の場合でも、図形データ項目の値は変更できます。また、[シェイプシート] ウィンドウの [図形データ] セクションも変更できます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCustProp] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockCustProp  <br/> |
   
プログラムから、インデックスによって [LockCustProp] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockCustProp** <br/> |
   

