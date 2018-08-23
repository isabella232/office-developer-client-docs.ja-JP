---
title: '[X] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: X 座標の位置に図形のローカル座標の中心となる操作タグ ボタンが配置されます。
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806801"
---
# <a name="x-cell-action-tags-section"></a>[X] セル ([操作タグ] セクション)

*X* -図形のローカル座標の内、操作タグ ボタンが配置される位置を調整します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>備考

[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> |スマート タグです。 *名*です。X スマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagX** <br/> |
   

