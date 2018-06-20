---
title: '[Alignment] セル ([Tabs] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
localization_priority: Normal
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: タブの整列方法を指定します。
ms.openlocfilehash: a2178c63d0005ee8b2f0c8ebcfbc25854a5b1567
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804762"
---
# <a name="alignment-cell-tabs-section"></a>[Alignment] セル ([Tabs] セクション)

タブの整列方法を指定します。
  
|**値**|**配置**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 左  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | 中央揃え  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | 右  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | 小数  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | カンマ  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Alignment] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | タブします。  *ij* *i および j =* < 1 > では、2、3  <br/> |
   
プログラムから、インデックスによって [Alignment] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTab** <br/> |
| 行インデックス:  <br/> |**visRowTab +***i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> | (*j* * 3) **+ visTabAlign** <br/> |
   

