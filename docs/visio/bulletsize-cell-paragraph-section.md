---
title: '[BulletSize] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: 箇条書きのサイズを指定します。
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804922"
---
# <a name="bulletsize-cell-paragraph-section"></a>[BulletSize] セル ([段落] セクション)

箇条書きのサイズを指定します。 
  
## <a name="remarks"></a>備考

この値は、定義済みの箇条書きまたはユーザー設定の箇条書きに対して、パーセントか特定の値のいずれかを指定できます。 
  
値がゼロ (0) の場合は、行頭文字は、段落の最初の文字と同じフォント サイズ。 値がパーセント値の場合は、行頭文字、段落の最初の文字のフォント サイズに対する割合でサイズが。 負の値は、パーセンテージとして扱われます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Para.BulletFontSize [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [BulletSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visBulletFontSize** <br/> |
   

