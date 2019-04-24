---
title: DisplayMode セル (Action Tags セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: ユーザーがタグの上にポインターを移動したとき、図形を選択したとき、または常に [アクション] タグを表示するかどうかを指定します。
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332733"
---
# <a name="displaymode-cell-action-tags-section"></a>DisplayMode セル (Action Tags セクション)

ユーザーがタグの上にポインターを移動したとき、図形を選択したとき、または常に [アクション] タグを表示するかどうかを指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**表示モード**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | タグ上でマウスを一時停止したときに表示されます (既定値)。  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1-d  <br/> | 図形を選択したときに表示します。  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| pbm-2  <br/> | 常に表示します。  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>解説

アクション タグは、印刷時や発行時には表示されません。 
  
ページに対してアクション タグが定義されていて、このセルの値が 1 の場合、ページは選択できないためタグは表示されません。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [DisplayMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | タグ.  *名前*です。DisplayMode の場合は、SmartTags。 *name*は、アクションタグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagDisplayMode** <br/> |
   

