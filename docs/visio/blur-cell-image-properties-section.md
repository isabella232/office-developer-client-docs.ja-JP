---
title: '[Blur] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
ms.localizationpriority: medium
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。
ms.openlocfilehash: 417a381a43de1e757dccebb1071f1b928ed02592
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59613122"
---
# <a name="blur-cell-image-properties-section"></a>[Blur] セル ([Image Properties] セクション)

ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Blur] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Blur  <br/> |
   
プログラムから、インデックスによって [Blur] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**visImageBlur** <br/> |
   

