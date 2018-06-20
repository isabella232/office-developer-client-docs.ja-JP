---
title: '[ObjType] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: オブジェクトを判断するかどうか配置可能なまたは図でルーティング可能な図形をレイアウトするのには、[レイアウトの構成] ダイアログ ボックスを使用するとします。
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805949"
---
# <a name="objtype-cell-miscellaneous-section"></a>[ObjType] セル ([Miscellaneous] セクション)

オブジェクトを判断するかどうか配置可能なまたは図でルーティング可能な図形をレイアウトするのには、[**レイアウトの構成**] ダイアログ ボックスを使用するとします。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |既定値です。図面のコンテキストに基づいて決定されます。  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |図形は配置可能です。  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |図形は迂回可能です。ただし 1 次元 (1-D) 図形でなければなりません。  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |図形は、配置も迂回もできません。  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |グループには、配置可能/迂回可能な図形が含まれます。  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>備考

既定では、なしの数式を 0 に評価されると、図形、図形のコンテキストに応じて配置できるかどうかをアプリケーションが決定されることを意味する [objtype] セルを設定します。 単純な四角形を描画する場合、[objtype] セルの値は 0 です。 四角形を別の図形に接続する**コネクタ**ツールを使用する場合、Visio は 1 (配置可能) に四角形の [objtype] セルの値をリセットします。 
  
[Objtype] セルの値は、値の組み合わせにできます。 配置可能ではないビットが設定されている場合 (&amp;H4)、ただし、それよりも優先グループの値を除くその他の値 (&amp;H8)。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [objtype] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[Objtype]  <br/> |
   
プログラムから、インデックスによって [objtype] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visLOFlags** <br/> |
   

