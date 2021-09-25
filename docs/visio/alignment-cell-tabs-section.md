---
title: '[Alignment] セル ([Tabs] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm35
ms.localizationpriority: medium
ms.assetid: 84234177-a2df-6acc-2761-230bc5d12627
description: タブの整列方法を指定します。
ms.openlocfilehash: 5ec858ecff9222feccebdc84c520b7f3f9ec819f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578278"
---
# <a name="alignment-cell-tabs-section"></a>[Alignment] セル ([Tabs] セクション)

タブの整列方法を指定します。
  
|**値**|**Alignment**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | Left  <br/> |**visTabStopLeft** <br/> |
| 1  <br/> | 中央  <br/> |**visTabStopCenter** <br/> |
| 2  <br/> | 右  <br/> |**visTabStopRight** <br/> |
| 3  <br/> | 10 進数  <br/> |**visTabStopDecimal** <br/> |
| 4   <br/> | カンマ  <br/> |**visTabStopComma** <br/> |
   
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
   

