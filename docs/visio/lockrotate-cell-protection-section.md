---
title: '[LockRotate] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
localization_priority: Normal
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: 2 次元図形をロックして、回転ハンドル、[左へ 90 度回転] コマンド、[右へ 90 度回転] コマンドによる回転操作ができないようにします。
ms.openlocfilehash: 450fe4786594472d018b705df4678fe636390ac3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805769"
---
# <a name="lockrotate-cell-protection-section"></a>[LockRotate] セル ([保護] セクション)

2 次元図形をロックして、回転ハンドル、[**左へ 90 度回転**] コマンド、[**右へ 90 度回転**] コマンドによる回転操作ができないようにします。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を回転できません。  <br/> |
| FALSE  <br/> | 図形を回転できます (既定値)。  <br/> |
   
## <a name="remarks"></a>備考

[LockRotate] セルを設定しても、1-D 図形は端点をドラッグして回転できます。1-D 図形の回転をロックするには、[LockWidth] セルをゼロ以外の値 (TRUE) に設定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockRotate] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockRotate  <br/> |
   
プログラムから、インデックスによって [LockRotate] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockRotate** <br/> |
   

