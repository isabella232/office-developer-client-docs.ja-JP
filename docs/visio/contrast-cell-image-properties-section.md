---
title: '[Contrast] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm200
localization_priority: Normal
ms.assetid: f0e4c644-c646-9649-c697-82feb02f5e29
description: ビットマップ イメージのコントラストを調整します。0 ～ 49% の範囲で値を入力するとイメージのコントラストが下がります。51 ～ 100% の範囲で値を入力するとイメージのコントラストが上がります。既定値は 50% です。
ms.openlocfilehash: 74a82fd9be49fcb9126c2b52bfcf25e0deb0e782
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805112"
---
# <a name="contrast-cell-image-properties-section"></a>[Contrast] セル ([画像のプロパティ] セクション)

ビットマップ イメージのコントラストを調整します。0 ～ 49% の範囲で値を入力するとイメージのコントラストが下がります。51 ～ 100% の範囲で値を入力するとイメージのコントラストが上がります。既定値は 50% です。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Contrast] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Contrast  <br/> |
   
プログラムから、インデックスによって [Contrast] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**visImageContrast** <br/> |
   

