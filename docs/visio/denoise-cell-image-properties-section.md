---
title: '[Denoise] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm225
localization_priority: Normal
ms.assetid: e305585f-f0d8-0494-91d4-0c76929dc170
description: ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。
ms.openlocfilehash: f08d09126a24935c0dd4dcda5e88fdd559c8d176
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805228"
---
# <a name="denoise-cell-image-properties-section"></a>[Denoise] セル ([画像のプロパティ] セクション)

ビットマップ画像からノイズを除去します。ノイズとは、カラー レベルが不規則に分散したピクセルのことです。既定値は 0% です。
  
## <a name="remarks"></a>備考

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
   

