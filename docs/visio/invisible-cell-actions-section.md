---
title: '[Invisible] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297243"
---
# <a name="invisible-cell-actions-section"></a>[Invisible] セル ([Actions] セクション)

アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |アクションはメニューに表示されません。  <br/> |
|FALSE  <br/> |アクションはメニューに表示されます (既定値)。  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション. *名前*です。Invisiblewhere アクション。  *name*は、Actions 行の名前です。  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visActionInvisible** <br/> |
   

