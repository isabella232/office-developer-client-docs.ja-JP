---
title: '[AsianFont] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033764
localization_priority: Normal
ms.assetid: 45bfaaaa-52cc-f8b4-68e7-8b99e5788ce1
description: アジア系文字を含むテキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。
ms.openlocfilehash: 1fbaa0b27a0c639519c302129142dcefe5708115
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804778"
---
# <a name="asianfont-cell-character-section"></a>[AsianFont] セル ([Character] セクション)

アジア系文字を含むテキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。 
  
## <a name="remarks"></a>注釈

アジア言語のフォントは、[**テキスト**] ダイアログ ボックス ([**ホーム**] タブの**フォント**にある矢印をグループ化] をクリック) の [**フォント**] タブに一覧表示されます。 このリストは、 **Microsoft Office 言語設定**] ダイアログ ボックスで、アジア言語や複雑なスクリプトの文字を含む言語を追加した場合にのみ表示されます。 ([**スタート**] ボタン [**すべてのプログラム**] をクリックして、 **Microsoft Office**、 **Microsoft Office ツール**] をクリックして、 **Microsoft Office 言語設定**] をクリックします。
  
番号 0 は、フォントが指定されていないことを意味します。ラテン フォントまたは既定値のフォントが必要な文字を含む場合はそれが使用されます。
  
取得する [asianfont] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.AsianFont [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [asianfont] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCharacterAsianFont** <br/> |
   

