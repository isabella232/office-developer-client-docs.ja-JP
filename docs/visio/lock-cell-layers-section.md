---
title: '[Lock] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm590
localization_priority: Normal
ms.assetid: 47bb268f-acdd-7369-716c-bd51a32b8a49
description: レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。
ms.openlocfilehash: f404fe15814de802f4f6bfcebfd2558cf10cc7eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805735"
---
# <a name="lock-cell-layers-section"></a>[Lock] セル ([Layers] セクション)

レイヤーに属する図形に対する選択操作や編集操作をロックするかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形をロックします。  <br/> |
|FALSE  <br/> |図形をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

**[レイヤー プロパティ**] ダイアログ ボックスで、**ロック**を選択することによって、この値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Lock] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Locked [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Lock] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visLayerLock** <br/> |
   

