---
title: '[ButtonFace] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
localization_priority: Normal
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: アクション タグ ボタンに表示されるボタン イメージの ID を示します。
ms.openlocfilehash: ca6be0a95b33e173219f4bdc1ba042c7162941b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804938"
---
# <a name="buttonface-cell-action-tags-section"></a>[ButtonFace] セル ([操作タグ] セクション)

アクション タグ ボタンに表示されるボタン イメージの ID を示します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>備考

ButtonFace] セルに含まれる文字列は、Microsoft Office のボタン イメージの ID を表します。 値が 0 (ゼロ) の標準のアクション タグの"i"情報ボタンの既定値を空白または![](media/InfoPS_ZA10180114.gif)。
  
ButtonFace] セルに使用できる Id は、 **CommandBarButton**オブジェクトの**FaceID**プロパティで使用される Id と同じです。 これらの Id の詳細については、MSDN の「コマンド バー ボタンのイメージを使用する」を検索してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。ButtonFace、スマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagButtonFace** <br/> |
   

