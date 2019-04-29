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
ms.openlocfilehash: 4af7e590a7bd0733ad622f3df259aa6c01837c4b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406592"
---
# <a name="asianfont-cell-character-section"></a>[AsianFont] セル ([Character] セクション)

アジア系文字を含むテキストの書式設定に使用するフォントの番号が含まれます。フォント番号は、ユーザーのシステムにインストールされているフォントによって異なります。 
  
## <a name="remarks"></a>注釈

アジア系フォントの一覧は、[**テキスト**] ダイアログ ボックスの [**フォント**] タブにあります (このタブを開くには、[**ホーム**] タブの [**フォント**] グループの矢印をクリックします)。この一覧が表示されるのは、[**Microsoft Office 言語設定**] ダイアログ ボックスにアジア系の文字または合成テキストが含まれている言語を追加した場合だけです (このダイアログ ボックスを開くには、[**スタート**] ボタンをクリックし、[**すべてのプログラム**]、[**Microsoft Office**]、[**Microsoft Office ツール**]、[**Microsoft Office 言語設定**] の順にクリックします)。
  
番号 0 は、フォントが指定されていないことを意味します。ラテン フォントまたは既定値のフォントが必要な文字を含む場合はそれが使用されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AsianFont] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[asianfont] [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [AsianFont] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCharacterAsianFont** <br/> |
   

