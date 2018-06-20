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
description: データ型が Date のときに、テキスト フィールドに使用するカレンダーを指定します。
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804925"
---
# <a name="calendar-cell-text-fields-section"></a>[Calendar] セル ([Text Fields] セクション)

データ型が Date のときに、テキスト フィールドに使用するカレンダーを指定します。
  
## <a name="remarks"></a>備考

使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、予定表のセルへの参照を名前によって取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Fields.Calendar [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [calendar] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionTextField** <br/> |
| 行インデックス:  <br/> |**visRowField** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visFieldCalendar** <br/> |
   

