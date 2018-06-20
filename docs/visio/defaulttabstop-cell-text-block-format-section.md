---
title: '[DefaultTabstop] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: テキスト ブロックの既定のタブ位置の間隔を指定します。
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805214"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a>[DefaultTabstop] セル ([Text Block Format] セクション)

テキスト ブロックの既定のタブ位置の間隔を指定します。 
  
## <a name="remarks"></a>注釈

既定値は、英国単位で図面を作成した場合は 0.5 インチ、メートル法単位の場合は 1.5 cm になります。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DefaultTabstop] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DefaultTabstop  <br/> |
   
プログラムから、インデックスによって [DefaultTabstop] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowText** <br/> |
|セル インデックス:  <br/> |**visTxtBlkDefaultTabStop** <br/> |
   

