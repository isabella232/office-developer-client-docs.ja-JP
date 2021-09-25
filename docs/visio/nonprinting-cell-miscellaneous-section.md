---
title: '[NonPrinting] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
ms.localizationpriority: medium
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: 選択した図形の印刷のオン/オフを切り替えます。
ms.openlocfilehash: f19e6f9e1c3ca140a16ac9ad8e5733ba70c3868c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573846"
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
   

