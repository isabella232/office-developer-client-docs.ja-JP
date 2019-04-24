---
title: '[ComplexScriptFont] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60034
localization_priority: Normal
ms.assetid: e1cf9e97-101b-384f-65fe-0169c89dfccc
description: 合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。
ms.openlocfilehash: 5ec8deb59b875a01592b6d7b652204089ecf11e0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359382"
---
# <a name="complexscriptfont-cell-character-section"></a>[ComplexScriptFont] セル ([Character] セクション)

合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。 
  
## <a name="remarks"></a>解説

コンプレックススクリプトのフォントサイズは、[**テキスト**] ダイアログボックスの [**フォント**] タブに表示されます ([**ホーム**] タブの [**フォント**] で矢印をクリック)。 この一覧は、[ **Microsoft Office 言語設定**] ダイアログボックスで、アジアまたはコンプレックススクリプト文字を含む言語を追加した場合にのみ表示されます。 ([**スタート**]、 **[すべてのプログラム**]、[ **microsoft office**]、[ **microsoft office ツール**]、[ **microsoft office の言語設定**] の順にクリックします。
  
番号 0 (ゼロ) は、フォントが指定されていないことを意味します。 ラテン フォントまたは既定のフォントが使われます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |文字 complexscriptfont [ *i* ] = <1> ** 、2、3...  <br/> |
   
プログラムから、インデックスによって [ComplexScriptFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

