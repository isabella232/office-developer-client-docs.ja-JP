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
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346152"
---
# <a name="flyoutchild-cell-actions-section"></a>[FlyoutChild] セル ([Actions] セクション)

行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FlyoutChild] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション. *名前*です。FlyoutChildwhere アクション。  *name*は、Actions 行の名前です。  <br/> |
   
プログラムから、インデックスによって [FlyoutChild] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visActionFlyoutChild** <br/> |
   

