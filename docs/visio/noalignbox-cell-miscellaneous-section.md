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
ms.openlocfilehash: 2ff9f051df54f4d424589332b9fbaea973552edc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435881"
---
# <a name="noalignbox-cell-miscellaneous-section"></a>[NoAlignBox] セル ([Miscellaneous] セクション)

選択した図形の選択範囲の表示/非表示を切り替えます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を選択するときに選択範囲が表示されません。  <br/> |
| FALSE  <br/> | 図形を選択するときに選択範囲が表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** を使用したプログラムから、名前によって [NoAlignBox] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [noalignbox]  <br/> |
   
プログラムから、インデックスによって [NoAlignBox] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNoAlignBox** <br/> |
   

