---
title: '[NoLine] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: パスの境界に線を描画するかどうかを指定します。
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805918"
---
# <a name="noline-cell-geometry-section"></a>[NoLine] セル ([図形座標] セクション)

パスの境界に線を描画するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 塗りつぶし領域の境界になっているパスの境界に線を描画しません。  <br/> |
| FALSE  <br/> | パスの境界に線を描画します。  <br/> |
   
## <a name="remarks"></a>備考

線の色を白に変更すると、白い背景では見えなくなりますが、線は存在しています。このセルの値を TRUE に設定すると、線は描画されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoLine] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。[Noline]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [NoLine] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoLine** <br/> |
   

