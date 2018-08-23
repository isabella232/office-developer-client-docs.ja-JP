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
ms.openlocfilehash: 0aae3a22be26f206763f18107eaced74f1078503
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805057"
---
# <a name="complexscriptfont-cell-character-section"></a>[ComplexScriptFont] セル ([文字] セクション)

合成テキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。 
  
## <a name="remarks"></a>注釈

コンプレックス スクリプトのフォントのサイズは、[**テキスト**] ダイアログ ボックス ([**ホーム**] タブの**フォント**にある矢印をグループ化] をクリック) の [**フォント**] タブに一覧表示されます。 このリストは、 **Microsoft Office 言語設定**] ダイアログ ボックスで、アジア言語や複雑なスクリプトの文字を含む言語を追加した場合にのみ表示されます。 ([**スタート**] ボタン [**すべてのプログラム**] をクリックして、 **Microsoft Office**、 **Microsoft Office ツール**] をクリックして、 **Microsoft Office 言語設定**] をクリックします。
  
番号 0 (ゼロ) では、フォントが指定されていないことを示します。 ラテン フォントまたは既定のフォントが使用されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.ComplexScriptFont [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [ComplexScriptFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCharacterComplexScriptFont** <br/> |
   

