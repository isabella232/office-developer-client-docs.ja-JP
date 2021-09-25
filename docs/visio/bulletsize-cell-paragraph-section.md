---
title: '[BulletSize] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
ms.localizationpriority: medium
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: 箇条書きのサイズを指定します。
ms.openlocfilehash: 97f22bc3e4071757de1336dca2efd2b4f1e12c41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623545"
---
# <a name="bulletsize-cell-paragraph-section"></a>[BulletSize] セル ([Paragraph] セクション)

箇条書きのサイズを指定します。 
  
## <a name="remarks"></a>注釈

この値は、定義済みの箇条書きまたはユーザー設定の箇条書きに対して、パーセントか特定の値のいずれかを指定できます。 
  
値が 0 (0) の場合、箇条書きは段落の最初の文字と同じフォント サイズになります。 値がパーセントの場合、箇条書きは段落の最初の文字に指定したパーセントのフォント サイズになります。 負の数字はパーセントと見なします。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Para.BulletFontSize[  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [BulletSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visBulletFontSize** <br/> |
   

