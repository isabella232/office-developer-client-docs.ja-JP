---
title: '[Sharpen] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm910
localization_priority: Normal
ms.assetid: aa2bebfc-a6bb-a6b3-3ae9-8553f96b5738
description: ビットマップ イメージを鮮明にします。 既定値は 0% です。 イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。
ms.openlocfilehash: e519cf6e5a168b64b4bc8aa083843163a47525ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415923"
---
# <a name="sharpen-cell-image-properties-section"></a>[Sharpen] セル ([Image Properties] セクション)

ビットマップ イメージを鮮明にします。 既定値は 0% です。 イメージを鮮明にすると、隣接するピクセルのコントラストが上がり、イメージがはっきりと表示されます。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Sharpen] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Sharpen  <br/> |
   
プログラムから、インデックスによって [Sharpen] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス :  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス :  <br/> |**(esハー)** <br/> |
   

