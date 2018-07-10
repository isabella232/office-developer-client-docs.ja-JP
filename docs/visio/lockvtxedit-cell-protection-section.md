---
title: '[LockVtxEdit] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: 図形の頂点をロックします。ロックすると、頂点を編集できなくなります。
ms.openlocfilehash: 3766df62bb85e1470ad0fa46274b9bbbd96b8406
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805793"
---
# <a name="lockvtxedit-cell-protection-section"></a>[LockVtxEdit] セル ([Protection] セクション)

図形の頂点をロックします。ロックすると、頂点を編集できなくなります。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |頂点を編集できません。  <br/> |
|FALSE  <br/> |頂点を編集できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockVtxEdit] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockVtxEdit  <br/> |
   
プログラムから、インデックスによって [LockVtxEdit] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockVtxEdit** <br/> |
   
