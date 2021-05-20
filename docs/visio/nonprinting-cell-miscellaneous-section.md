---
title: '[NonPrinting] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: 選択した図形の印刷のオン/オフを切り替えます。
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437260"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>[NonPrinting] セル ([Miscellaneous] セクション)

選択した図形の印刷のオン/オフを切り替えます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 印刷は無効になりますが、図形は図面ウィンドウに表示されます。  <br/> |
| FALSE  <br/> | 印刷は有効になります。  <br/> |
   
## <a name="remarks"></a>注釈

ガイドを選択し、その [NonPrinting] セルの値を FALSE に設定すると、ガイドを印刷できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NonPrinting] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | NonPrinting  <br/> |
   
プログラムから、インデックスによって [NonPrinting] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNonPrinting** <br/> |
   

