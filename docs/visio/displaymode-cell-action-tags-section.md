---
title: DisplayMode セル (アクション タグのセクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: アクションのタグには、ユーザーがタグの上、ポインターを移動すると、図形が選択されている場合、またはすべての時間が表示されるかどうかを決定します。
ms.openlocfilehash: 4cb0666ca8de28247309de4fc0d2ff23e8b37d8a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805219"
---
# <a name="displaymode-cell-action-tags-section"></a>DisplayMode セル (アクション タグのセクション)

アクションのタグには、ユーザーがタグの上、ポインターを移動すると、図形が選択されている場合、またはすべての時間が表示されるかどうかを決定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**表示モード**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | タグ (デフォルト) の上にマウスを置いたときに表示されます。  <br/> |**visSmartTagDispModeMouseOver** <br/> |
| 1  <br/> | 図形を選択したときに表示します。  <br/> |**visSmartTagDispModeShapeSelected** <br/> |
| 2  <br/> | 常に表示します。  <br/> |**visSmartTagDispModeAlways** <br/> |
   
## <a name="remarks"></a>備考

アクション タグは、印刷時や発行時には表示されません。 
  
ページに対してアクション タグが定義されていて、このセルの値が 1 の場合、ページは選択できないためタグは表示されません。 
  
取得する DisplayMode] セルへの参照の名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。DisplayMode、スマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [DisplayMode] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagDisplayMode** <br/> |
   

