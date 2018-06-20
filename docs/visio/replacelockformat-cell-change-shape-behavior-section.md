---
title: '[ReplaceLockFormat] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 マスター シェイプの ReplaceLockFormat セルは、(1) は、TRUE に設定されている場合、マスター シェイプの書式設定の値はマスターによって置換される図形のすべてに対応する値を上書きします。
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806202"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>[ReplaceLockFormat] セル ([図形の動作の変更] セクション)

マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 マスター シェイプの**ReplaceLockFormat**セルは、(1) は、TRUE に設定されている場合、マスター シェイプの書式設定の値はマスターによって置換される図形のすべてに対応する値を上書きします。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |マスター シェイプの**ReplaceLockFormat**セルを TRUE に設定すると、マスター シェイプの書式設定の値は交換するため、マスター シェイプのすべての対応する値を上書きします。  <br/> |
|FALSE  <br/> |マスター シェイプの**ReplaceLockFormat**セルが FALSE に設定されている場合、置換後の図形には、置換操作後に古い図形のローカル書式設定値が含まれています。  <br/> |
   
## <a name="remarks"></a>備考

**ReplaceLockFormat**セルでは、マスター シェイプが図形の置換操作の実行中に次のセクションのセルのローカルの書式設定値を上書きするかどうかを決定します。 
  
- **塗りつぶしの書式**セクション 
    
- **行の書式**セクション 
    
- [**クイック スタイル**] 
    
- **テーマのプロパティ**] セクション 
    
- **グラデーションのプロパティ**] セクション 
    
- **傾斜面のプロパティ**] セクション 
    
- **その他のエフェクトのプロパティ**] セクション 
    
- **グラデーション終了位置の行**セクション 
    
- **グラデーション終了位置の設定**] セクション 
    
**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceLockFormat** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceLockFormat  <br/> |
   
プログラムから、インデックスによって [ **ReplaceLockFormat** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceLockFormat** <br/> |
   

