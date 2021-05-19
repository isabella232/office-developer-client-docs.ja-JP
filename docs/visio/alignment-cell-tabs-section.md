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
ms.openlocfilehash: 461357c9c838fb4c0e5b0159bf027dd6adce26f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425541"
---
# <a name="alignment-cell-tabs-section"></a>[Alignment] セル ([Tabs] セクション)

タブの整列方法を指定します。
  
|**値**|**Alignment**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | Left  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | 中央  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | 右  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | 10 進数  <br/> |**visTabStopDecimal** <br/> |
| 4  <br/> | カンマ  <br/> |**visTabStopComma** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Alignment] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | タブ。  *ij*            は  *i と j = <*  1>、2、3  <br/> |
   
プログラムから、インデックスによって [Alignment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTab** <br/> |
| 行インデックス:  <br/> |**visRowTab +** *i*            *=*  0, 1, 2...  <br/> |
| セル インデックス:  <br/> | (*j*  *3) **+ visTabAlign** <br/> |
   

