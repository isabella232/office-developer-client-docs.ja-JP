---
title: '[X] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
ms.localizationpriority: medium
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: アクション タグ ボタンを配置する図形のローカル座標の x 座標位置。
ms.openlocfilehash: 76b334daf087fd2fcacf1fd706cfb3186e87110c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603194"
---
# <a name="x-cell-action-tags-section"></a>[X] セル ([Action Tags] セクション)

アクション  *タグ*  ボタンを配置する図形のローカル座標の x 座標位置。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> |SmartTags。 *name*  .X は SmartTags です。 *name*  はアクション タグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagX** <br/> |
   

