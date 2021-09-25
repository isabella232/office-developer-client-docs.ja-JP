---
title: '[Denoise] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
ms.localizationpriority: medium
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。
ms.openlocfilehash: 40d9048cd24f0585c246436217f0ed5b515eb32a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559949"
---
# <a name="denoise-cell-image-properties-section"></a>[Denoise] セル ([Image Properties] セクション)

ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Denoise] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Denoise  <br/> |
   
プログラムから、インデックスによって [Denoise] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**visImageDenoise** <br/> |
   

