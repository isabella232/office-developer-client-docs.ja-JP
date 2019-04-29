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
ms.openlocfilehash: 38b01c4a0142c7eca2923ee9b13963eaa1a62830
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428439"
---
# <a name="complexscriptsize-cell-character-section"></a>[ComplexScriptSize] セル ([Character] セクション)

合成テキストの書式設定に使用するフォントのサイズです。 
  
## <a name="remarks"></a>注釈

コンプレックススクリプトのフォントサイズは、[**テキスト**] ダイアログボックスの [**フォント**] タブに表示されます ([**ホーム**] タブの [**フォント**] で矢印をクリック)。 この一覧は、[ **Microsoft Office 言語設定**] ダイアログボックスで、アジアまたはコンプレックススクリプト文字を含む言語を追加した場合にのみ表示されます。 ([**スタート**]、 **[すべてのプログラム**]、[ **microsoft office**]、[ **microsoft office ツール**]、[ **microsoft office の言語設定**] の順にクリックします。
  
この値には、明示的なポイント サイズまたはパーセントを入力することができます。パーセントを指定した場合、[Size] セルの値を基に値が設定されます。既定値の 0 (ゼロ) は 100% を意味します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ComplexScriptSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |文字 complexscriptsize [ *i* ] = <1> ** 、2、3...  <br/> |
   
プログラムから、インデックスによって [ComplexScriptSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCharacterComplexScriptSize** <br/> |
   

