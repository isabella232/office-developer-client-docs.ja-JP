---
title: '[Brightness] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
ms.localizationpriority: medium
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。
ms.openlocfilehash: 41615007b66a0b148c9166ee76126b935a5327c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578145"
---
# <a name="brightness-cell-image-properties-section"></a>[Brightness] セル ([Image Properties] セクション)

ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Brightness] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Brightness  <br/> |
   
プログラムから、インデックスによって [Brightness] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**visImageBrightness** <br/> |
   

