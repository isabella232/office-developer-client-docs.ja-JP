---
title: '[Calendar] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: データ型が Date のときに、テキストフィールドに使用するカレンダーを指定します。
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337500"
---
# <a name="calendar-cell-text-fields-section"></a>[Calendar] セル ([Text Fields] セクション)

データ型が Date のときに、テキストフィールドに使用するカレンダーを指定します。
  
## <a name="remarks"></a>解説

使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | フィールド。 *i* = ** <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visFieldCalendar** <br/> |
   

