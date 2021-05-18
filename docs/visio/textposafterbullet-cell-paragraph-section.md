---
title: '[TextPosAfterBullet] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: 段落の第 1 行目と箇条書き行頭文字の間の距離を表します。
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422153"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>[TextPosAfterBullet] セル ([Paragraph] セクション)

段落の第 1 行目と箇条書き行頭文字の間の距離を表します。 
  
## <a name="remarks"></a>注釈

この距離は、[IndFirst] セル内に含まれている距離 (既定の左インデント) に追加されます。この値は、図面の縮尺による影響を受けません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextPosAfterBullet] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Para.TextPosAfterBullet[ i ]*ここで、i* = <1>、2、3...   <br/> |
   
プログラムから、インデックスによって [TextPosAfterBullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visTextPosAfterBullet** <br/> |
   

