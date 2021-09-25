---
title: '[LockRotate] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm655
ms.localizationpriority: medium
ms.assetid: 2d97b31d-9008-307d-273a-1726007eeb34
description: 2 次元図形をロックして、回転ハンドル、[左へ 90 度回転] コマンド、[右へ 90 度回転] コマンドによる回転操作ができないようにします。
ms.openlocfilehash: e40ba399c2acc2650152bdcdd639b86a5cd650dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627969"
---
# <a name="lockrotate-cell-protection-section"></a>[LockRotate] セル ([Protection] セクション)

2 次元図形をロックして、回転ハンドル、[**左へ 90 度回転**] コマンド、[**右へ 90 度回転**] コマンドによる回転操作ができないようにします。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を回転できません。  <br/> |
| FALSE  <br/> | 図形を回転できます (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

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
   

