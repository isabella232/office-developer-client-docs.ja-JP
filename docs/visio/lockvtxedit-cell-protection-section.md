---
title: '[LockVtxEdit] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
ms.localizationpriority: medium
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: 図形の頂点をロックします。ロックすると、頂点を編集できなくなります。
ms.openlocfilehash: ca90a85a327f9f51380957bcdd3fd5c3ff4a6d36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612471"
---
# <a name="lockvtxedit-cell-protection-section"></a>[LockVtxEdit] セル ([Protection] セクション)

図形の頂点をロックします。ロックすると、頂点を編集できなくなります。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |頂点を編集できません。  <br/> |
|FALSE  <br/> |頂点を編集できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockVtxEdit] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockVtxEdit  <br/> |
   
プログラムから、インデックスによって [LockVtxEdit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockVtxEdit** <br/> |
   

