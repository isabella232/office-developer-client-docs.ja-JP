---
title: '[Style] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
ms.localizationpriority: medium
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: 図形のテキスト ブロック内にあるテキストの範囲に適用される文字の書式を表示します。
ms.openlocfilehash: 4171ceac4ea092b3ed70bb06c11b1113d61ef1b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603390"
---
# <a name="style-cell-character-section"></a>[Style] セル ([Character] セクション)

図形のテキスト ブロック内にあるテキストの範囲に適用される文字の書式を表示します。
  
|**スタイル**|**値**|**オートメーション定数**|
|:-----|:-----|:-----|
| 太字  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| 斜体  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| 下線  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| 小型英文字  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>注釈

[Character] セクションに複数の行が含まれる場合は、[Style] セルには、図形のテキストのサブ範囲に適用される書式設定情報が表示されます。複数の行が含まれない場合は、このセルには、すべての図形のテキストに対する書式設定情報が表示されます。
  
この値はバイナリ数値で表示され、バイナリ数値を構成する個々の値によって文字スタイルが決まります。 たとえば、値 3 は、斜体と太字の両方で書式設定されたテキストを表します。 [スタイル] の値が 0 の場合は、テキストはプレーン テキストつまり書式設定なしになります。 ブール型 BIT 関数を使用して、特定の形式をテスト \* できます。 これらの関数の詳細については、プログラミングに関するマニュアルを参照してください。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Style] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Char.Style[  *i*  ]  *ここで、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Style] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCharacterStyle** <br/> |
   
 *例* 
  
ある図形の [Character] セクションの先頭行にある [Color] セルが、次の数式に設定されているとします。
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
図形のテキスト上にある最初の文字が太字の場合は、最初の Character プロパティ行の対象となるテキストは青 (4) になります。太字以外の場合は、テキストは緑 (3) になります。この例では、既定の色が有効であるものと仮定します。
  
次の例は、プログラムの中で [Style] セルを設定するものです。先頭のステートメントは、名前によって [Style] セルを参照します。2 番目のステートメントは、インデックスによって [Style] セルを参照します。どちらのステートメントも、図形の [Character] セクションの第 2 行の対象となるテキストに対して斜体を適用します。
  

