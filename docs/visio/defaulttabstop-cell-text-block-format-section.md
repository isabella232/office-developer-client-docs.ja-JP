---
title: '[DefaultTabstop] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
ms.localizationpriority: medium
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: テキスト ブロックの既定のタブ位置の間隔を指定します。
ms.openlocfilehash: 10589f110ec1121fd04bdd3caea6ca876bbfc3c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628480"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>[DefaultTabstop] セル ([Text Block Format] セクション)

テキスト ブロックの既定のタブ位置の間隔を指定します。 
  
## <a name="remarks"></a>注釈

既定値は、英国単位で図面を作成した場合は 0.5 インチ、メートル法単位の場合は 1.5 cm になります。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DefaultTabstop] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DefaultTabstop  <br/> |
   
プログラムから、インデックスによって [DefaultTabstop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowText** <br/> |
|セル インデックス:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

