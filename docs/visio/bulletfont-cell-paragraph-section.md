---
title: '[BulletFont] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
ms.localizationpriority: medium
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。
ms.openlocfilehash: 32c7240ac9cf44c7e37ba5fee003f0b5bc876bd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603803"
---
# <a name="bulletfont-cell-paragraph-section"></a>[BulletFont] セル ([Paragraph] セクション)

ユーザー設定の箇条書き文字列を指定し、[Bullet] セルの値がゼロ以外のとき、テキストの書式設定に使用するフォントの番号を表します。 
  
## <a name="remarks"></a>注釈

フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。値が 0 でユーザー設定の箇条書き文字列がある場合、使用されるフォントは、段落の最初の文字のフォントと同じです。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BulletFont] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Para.BulletFont[ i ]*ここで**、i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [BulletFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionParagraph** <br/> |
| 行インデックス:  <br/> |**visRowParagraph**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visBulletFont** <br/> |
   

