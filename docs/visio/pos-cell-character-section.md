---
title: '[Pos] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm805
localization_priority: Normal
ms.assetid: c02186ce-6a20-fbe7-588d-d64c3ea4dec4
description: 基線に対する、図形のテキストの位置を指定します。
ms.openlocfilehash: 50ce5a3f7caf3e716f430aa08326281c8dc847f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806091"
---
# <a name="pos-cell-character-section"></a>[Pos] セル ([文字] セクション)

基線に対する、図形のテキストの位置を指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 標準の位置  <br/> |**visPosNormal** <br/> |
| 1  <br/> | 上付き  <br/> |**visPosSuper** <br/> |
| 2  <br/> | 下付き  <br/> |**visPosSub** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Pos] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Char.Pos [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Pos] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionCharacter** <br/> |
| 行インデックス:  <br/> |**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCharacterPos** <br/> |
   

