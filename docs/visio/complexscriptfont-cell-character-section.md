---
title: '[ComplexScriptFont] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
ms.localizationpriority: medium
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: 合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。
ms.openlocfilehash: c5bba5bcc8881717647f74127d745286615fe660
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566018"
---
# <a name="complexscriptfont-cell-character-section"></a>[ComplexScriptFont] セル ([Character] セクション)

合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。 
  
## <a name="remarks"></a>注釈

複雑なスクリプトのフォント サイズは、[テキスト] ダイアログボックスの [フォント] タブに表示されます ([ホーム] タブの [フォント] グループの矢印 **をクリック** します)。  このリストは、[言語の基本設定] ダイアログ ボックスで、アジア文字または複雑なスクリプト文字を含む言語を追加 **Microsoft Office表示されます**。 ([**スタート] ボタン、[** すべてのプログラム **]** の順にクリックし、[Microsoft Office]**をクリック** し、[Microsoft Office **ツール**] をクリックし、[言語の基本設定] Microsoft Office **クリックします**。
  
番号 0 (ゼロ) は、フォントが指定されていないことを意味します。 ラテン フォントまたは既定のフォントが使われます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.ComplexScriptFont[ i ]*ここで、i* = <1>、2、3...   <br/> |
   
プログラムから、インデックスによって [ComplexScriptFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

