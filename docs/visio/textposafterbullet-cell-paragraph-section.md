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
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806631"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>[TextPosAfterBullet] セル ([段落] セクション)

段落の第 1 行目と箇条書き行頭文字の間の距離を表します。 
  
## <a name="remarks"></a>備考

この距離は、[IndFirst] セル内に含まれている距離 (既定の左インデント) に追加されます。この値は、図面の縮尺による影響を受けません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextPosAfterBullet] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Para.TextPosAfterBullet [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [TextPosAfterBullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visTextPosAfterBullet** <br/> |
   

