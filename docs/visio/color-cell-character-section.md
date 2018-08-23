---
title: '[Color] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: 図形のテキストに使用する色を指定します。
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805007"
---
# <a name="color-cell-character-section"></a>[Color] セル ([文字] セクション)

図形のテキストに使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
独自の色を入力するには、RGB または HSL 関数を使用します。 その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。 数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。 
  
テキストの色の透過性を設定するには、[Transparency] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Char.Color [ *i* ]、 *i* = < 1 > では、2、3、.  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
|行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0、1、2、.  <br/> |
|セル インデックス:  <br/> |**visCharacterColor** <br/> |
   

