---
title: '[NoFill] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm710
localization_priority: Normal
ms.assetid: 0ba7f6da-681b-b749-fe72-afbca23d7e16
description: パスに塗りつぶしを適用するかどうかを指定します。
ms.openlocfilehash: 3f5bab76fc38b6e82aeaeee45b75bd733afdbd26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805923"
---
# <a name="nofill-cell-geometry-section"></a>[NoFill] セル ([図形座標] セクション)

パスに塗りつぶしを適用するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形の他のパスが塗りつぶされていても、このパスは塗りつぶされません。  <br/> |
| FALSE  <br/> | パスが閉じていない場合でも、図形の塗りつぶしがこのパスに適用されます。  <br/> |
   
## <a name="remarks"></a>備考

図形の塗りつぶしパターンをゼロ (0) に設定すると、すべてのパスに対して塗りつぶしが適用されません。図形内にある特定のパスに対して塗りつぶしを適用しない場合に、このセルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoFill] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。[Nofill]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [NoFill] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoFill** <br/> |
   

