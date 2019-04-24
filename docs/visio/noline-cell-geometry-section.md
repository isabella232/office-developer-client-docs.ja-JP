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
ms.openlocfilehash: ad3744ae8deb4ffb4dd2282e50590439c4b218a4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357282"
---
# <a name="noline-cell-geometry-section"></a>[NoLine] セル ([Geometry] セクション)

パスの境界に線を描画するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 塗りつぶし領域の境界になっているパスの境界に線を描画しません。  <br/> |
| FALSE  <br/> | パスの境界に線を描画します。  <br/> |
   
## <a name="remarks"></a>解説

線の色を白に変更すると、白い背景では見えなくなりますが、線は存在しています。このセルの値を TRUE に設定すると、線は描画されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoLine] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ジオメトリ*i*noline *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [NoLine] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス :  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoLine** <br/> |
   

