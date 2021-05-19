---
title: '[DisplayMode] セル ([アクション タグ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: ユーザーがポインターをタグの上に移動した場合、図形が選択されている場合、またはすべての時刻にアクション タグが表示されるかどうかを指定します。
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415818"
---
# <a name="displaymode-cell-action-tags-section"></a>[DisplayMode] セル ([アクション タグ] セクション)

ユーザーがポインターをタグの上に移動した場合、図形が選択されている場合、またはすべての時刻にアクション タグが表示されるかどうかを指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**表示モード**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | タグの上でマウスを一時停止すると表示されます (既定値)。  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | 図形を選択したときに表示します。  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | 常に表示します。  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>注釈

アクション タグは、印刷時や発行時には表示されません。 
  
ページに対してアクション タグが定義されていて、このセルの値が 1 の場合、ページは選択できないためタグは表示されません。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [DisplayMode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SmartTags。  *name*  .SmartTags の DisplayMode。 *name*  はアクション タグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagDisplayMode** <br/> |
   

