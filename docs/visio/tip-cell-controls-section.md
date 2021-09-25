---
title: '[Tip] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
ms.localizationpriority: medium
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを置いたときに表示されます。セルではヒントの文字列は自動的に引用符で囲まれますが、ツール ヒントには引用符は表示されません。
ms.openlocfilehash: 834583eece5c71d42218e67411944fee11279f65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569889"
---
# <a name="tip-cell-controls-section"></a>[Tip] セル ([Controls] セクション)

ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを置いたときに表示されます。セルではヒントの文字列は自動的に引用符で囲まれますが、ツール ヒントには引用符は表示されません。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Tip] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | コントロール。  *name*  .Tipwhere コントロール。  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [Tip] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCtlTip** <br/> |
   

