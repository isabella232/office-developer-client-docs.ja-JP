---
title: '[SortKey] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806562"
---
# <a name="sortkey-cell-actions-section"></a>[SortKey] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューに表示されるアクションの順序を指定する数字です。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

ショートカット メニューまたはアクション タグ メニューのアクションは、最小の数値から最大の数値の順に並べられ、最小の数値がメニューの一番上に表示されます。2 つのアクション行で [SortKey] セルの値が同じ場合は、物理的な行の順序で並べられます。既定値は 0 (ゼロ) です。
  
取得する [sortkey] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。SortKeywhere アクションです。  *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [sortkey] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionSortKey** <br/> |
   

