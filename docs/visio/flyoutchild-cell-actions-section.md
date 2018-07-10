---
title: '[FlyoutChild] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: 行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805407"
---
# <a name="flyoutchild-cell-actions-section"></a>[FlyoutChild] セル ([Actions] セクション)

行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。 
  
## <a name="remarks"></a>備考

参照を取得する FlyoutChild のセルに名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次の手順を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。FlyoutChildwhere アクションです。  *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [FlyoutChild] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionFlyoutChild** <br/> |
   
