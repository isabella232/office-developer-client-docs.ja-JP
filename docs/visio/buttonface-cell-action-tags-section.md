---
title: '[ButtonFace] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60026
ms.localizationpriority: medium
ms.assetid: 26f370e1-5193-f47d-7b60-3597975be650
description: アクション タグ ボタンに表示されるボタン イメージの ID を示します。
ms.openlocfilehash: b445a35fe6582b07fd988eacec24725d36466aca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578131"
---
# <a name="buttonface-cell-action-tags-section"></a>[ButtonFace] セル ([Action Tags] セクション)

アクション タグ ボタンに表示されるボタン イメージの ID を示します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[ButtonFace] セル内の文字列は Microsoft Office のボタン イメージの ID を示します。 値が 0 (ゼロ) または空白の既定値は、標準アクション タグ "i" info ボタン ![標準アクション タグ "i" info ボタン](media/InfoPS_ZA10180114.gif).
  
[ButtonFace] セルに使用される ID は、 **CommandBarButton** オブジェクトの  **FaceID** プロパティで使用される ID と同じです。 これらの ID の詳細については、MSDN で "コマンド バー ボタンイメージを操作する" を検索します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SmartTags。  *name*  .ButtonFace where SmartTags. *name*  はアクション タグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス :  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス :  <br/> |**visSmartTagButtonFace** <br/> |
   

