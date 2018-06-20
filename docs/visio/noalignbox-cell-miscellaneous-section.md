---
title: '[NoAlignBox] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: 選択した図形の選択範囲の表示/非表示を切り替えます。
ms.openlocfilehash: c8e5fe28197a72b4cdb5306732dd155dc8f4f810
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805916"
---
# <a name="noalignbox-cell-miscellaneous-section"></a>[NoAlignBox] セル ([Miscellaneous] セクション)

選択した図形の選択範囲の表示/非表示を切り替えます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を選択するときに選択範囲が表示されません。  <br/> |
| FALSE  <br/> | 図形を選択するときに選択範囲が表示されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[NoAlignBox] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | NoAlignBox  <br/> |
   
プログラムから、インデックスによって [NoAlignBox] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNoAlignBox** <br/> |
   

