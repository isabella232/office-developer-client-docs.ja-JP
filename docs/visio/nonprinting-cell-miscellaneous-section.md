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
ms.openlocfilehash: ab00914a9c59cfe94b3f7273f89684f43328b4d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805922"
---
# <a name="nonprinting-cell-miscellaneous-section"></a>[NonPrinting] セル ([その他] セクション)

選択した図形の印刷のオン/オフを切り替えます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 印刷は無効になりますが、図形は図面ウィンドウに表示されます。  <br/> |
| FALSE  <br/> | 印刷は有効になります。  <br/> |
   
## <a name="remarks"></a>備考

ガイドを選択し、その [NonPrinting] セルの値を FALSE に設定すると、ガイドを印刷できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NonPrinting] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 印刷できません。  <br/> |
   
プログラムから、インデックスによって [NonPrinting] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNonPrinting** <br/> |
   

