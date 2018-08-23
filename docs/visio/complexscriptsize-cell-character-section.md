---
title: '[ComplexScriptSize] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033768
localization_priority: Normal
ms.assetid: f58687d7-2ba4-ff77-0bcc-3106867d89de
description: 合成テキストの書式設定に使用するフォントのサイズです。
ms.openlocfilehash: 4867ab57fa59b3a5e76598108fbb92b9bbab7913
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805062"
---
# <a name="complexscriptsize-cell-character-section"></a>[ComplexScriptSize] セル ([文字] セクション)

合成テキストの書式設定に使用するフォントのサイズです。 
  
## <a name="remarks"></a>注釈

コンプレックス スクリプトのフォントのサイズは、[**テキスト**] ダイアログ ボックス ([**ホーム**] タブの**フォント**にある矢印をグループ化] をクリック) の [**フォント**] タブに一覧表示されます。 このリストは、 **Microsoft Office 言語設定**] ダイアログ ボックスで、アジア言語や複雑なスクリプトの文字を含む言語を追加した場合にのみ表示されます。 ([**スタート**] ボタン [**すべてのプログラム**] をクリックして、 **Microsoft Office**、 **Microsoft Office ツール**] をクリックして、 **Microsoft Office 言語設定**] をクリックします。
  
この値には、明示的なポイント サイズまたはパーセントを入力することができます。パーセントを指定した場合、[Size] セルの値を基に値が設定されます。既定値の 0 (ゼロ) は 100% を意味します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.ComplexScriptSize [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [ComplexScriptSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

