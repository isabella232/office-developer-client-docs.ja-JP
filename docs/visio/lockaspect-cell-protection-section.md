---
title: '[LockAspect] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
ms.localizationpriority: medium
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: 図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。
ms.openlocfilehash: ee7ca3df9cce5f11a83fb8665d9db93d21f3c27e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628023"
---
# <a name="lockaspect-cell-protection-section"></a>[LockAspect] セル ([Protection] セクション)

図形の縦横比をロックします。ロックすると、図形のサイズを変更するときに縦横比が維持されます。上下、左右のいずれか一方向だけサイズを変更することができなくなります。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 縦横比をロックします。  <br/> |
| FALSE  <br/> | 縦横比をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockAspect] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockAspect  <br/> |
   
プログラムから、インデックスによって [LockAspect] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockAspect** <br/> |
   

