---
title: '[ComplexScriptSize] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
ms.localizationpriority: medium
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: 合成テキストの書式設定に使用するフォントのサイズです。
ms.openlocfilehash: 8d810cecb7f9bd1d80895892a362d808f8adc3f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608474"
---
# <a name="complexscriptsize-cell-character-section"></a>[ComplexScriptSize] セル ([Character] セクション)

合成テキストの書式設定に使用するフォントのサイズです。 
  
## <a name="remarks"></a>注釈

複雑なスクリプトのフォント サイズは、[テキスト] ダイアログボックスの [フォント] タブに表示されます ([ホーム] タブの [フォント] グループの矢印 **をクリック** します)。  このリストは、[言語の基本設定] ダイアログ ボックスで、アジア文字または複雑なスクリプト文字を含む言語を追加 **Microsoft Office表示されます**。 ([**スタート] ボタン、[** すべてのプログラム **]** の順にクリックし、[Microsoft Office]**をクリック** し、[Microsoft Office **ツール**] をクリックし、[言語の基本設定] Microsoft Office **クリックします**。
  
この値には、明示的なポイント サイズまたはパーセントを入力することができます。パーセントを指定した場合、[Size] セルの値を基に値が設定されます。既定値の 0 (ゼロ) は 100% を意味します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.ComplexScriptSize[ i ]*ここで、i* = <1>、2、3...   <br/> |
   
プログラムから、インデックスによって [ComplexScriptSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

