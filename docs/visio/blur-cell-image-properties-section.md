---
title: '[Blur] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm115
localization_priority: Normal
ms.assetid: 8b077cdb-6036-4f77-dc20-a476bb75b0f7
description: ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。
ms.openlocfilehash: 14a50f2015b2b24d7e41f5d11018a749d089fc37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804916"
---
# <a name="blur-cell-image-properties-section"></a>[Blur] セル ([Image Properties] セクション)

ビットマップ イメージをぼかしたり、色をやわらげたりします。既定値は 0% です。
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [Blur] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Blur  <br/> |
   
プログラムから、インデックスによって [Blur] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**visImageBlur** <br/> |
   

