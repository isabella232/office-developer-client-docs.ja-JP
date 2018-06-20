---
title: '[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: 図形のテキストが 3-d 図形の回転を無視するかどうかを示します。 2 次元の回転には適用されません。
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805644"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>[KeepTextFlat] セル ([3-D 回転のプロパティ] セクション)

図形のテキストが 3-d 図形の回転を無視するかどうかを示します。 2 次元の回転には適用されません。 
  
****

|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形のジオメトリを使用して図形のテキストが回転しません。  <br/> |
|FALSE  <br/> |図形のジオメトリを回転する図形のテキストが変換されます。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **KeepTextFlat** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |KeepTextFlat  <br/> |
   
プログラムから、インデックスによって [ **KeepTextFlat** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRow3DRotationProperties** <br/> |
|セル インデックス:  <br/> |**visKeepTextFlat** <br/> |
   

