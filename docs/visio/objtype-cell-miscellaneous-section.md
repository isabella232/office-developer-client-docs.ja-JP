---
title: '[ObjType] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
ms.localizationpriority: medium
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: '[レイアウトの構成] ダイアログ ボックスを使用して図形をレイアウトするときに、図面上のオブジェクトが配置可能かどうか、または迂回可能かどうかを指定します。'
ms.openlocfilehash: 22a34d21cf383ea12c05bb43588702335ae593ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608187"
---
# <a name="objtype-cell-miscellaneous-section"></a>[ObjType] セル ([Miscellaneous] セクション)

[**レイアウトの構成**] ダイアログ ボックスを使用して図形をレイアウトするときに、図面上のオブジェクトが配置可能かどうか、または迂回可能かどうかを指定します。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|&amp;H0  <br/> |既定値です。図面のコンテキストに基づいて決定されます。  <br/> |**visLOFlagsVisDecides** <br/> |
|&amp;H1  <br/> |図形は配置可能です。  <br/> |**visLOFlagsPlacable** <br/> |
|&amp;H2  <br/> |図形は迂回可能です。ただし 1 次元 (1-D) 図形でなければなりません。  <br/> |**visLOFlagsRoutable** <br/> |
|&amp;H4  <br/> |図形は、配置も迂回もできません。  <br/> |**visLOFlagsDont** <br/> |
|&amp;H8  <br/> |グループには、配置可能/迂回可能な図形が含まれます。  <br/> |**visLOFlagsPNRGroup** <br/> |
   
## <a name="remarks"></a>注釈

既定では、図形の [ObjType] セルは "No Formula" に設定されます。これは 0 と評価され、図形が配置可能かどうかはコンテキストに応じて決定されます。たとえば、単純な四角形を描画すると、[ObjType] セルの値は 0 になります。[**コネクタ**] ツールを使用して、この四角形を別の図形に接続すると、四角形の [ObjType] セルの値は 1 (配置可能) になります。 
  
[ObjType] セルには、値を組み合わせて指定することもできます。 ただし、非配置可能ビットが設定されている場合 ( H4) は、グループ値 ( H8) を除く他の値よりも &amp; &amp; 優先されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ObjType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ObjType  <br/> |
   
プログラムから、インデックスによって [ObjType] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visLOFlags** <br/> |
   

