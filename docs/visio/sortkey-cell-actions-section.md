---
title: '[SortKey] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
ms.localizationpriority: medium
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。
ms.openlocfilehash: 563bb5213d2fe1e43c16648ecef0955c779a4348
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598011"
---
# <a name="sortkey-cell-actions-section"></a>[SortKey] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

ショートカット メニューまたはアクション タグ メニューのアクションは、最小の数値から最大の数値の順に並べられ、最小の数値がメニューの一番上に表示されます。2 つのアクション行で [SortKey] セルの値が同じ場合は、物理的な行の順序で並べられます。既定値は 0 (ゼロ) です。
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [SortKey] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション。 *name*  .SortKeywhere アクション。  *name*  は [アクション] 行の名前です。  <br/> |
   
プログラムから、インデックスによって [SortKey] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visActionSortKey** <br/> |
   

