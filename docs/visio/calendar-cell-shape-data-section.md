---
title: '[Calendar] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: データ型が Date のとき図形データに使用するカレンダーを指定します。
ms.openlocfilehash: 502ecd8a028c4c0d9841bbd3e0ed369f73bd6b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804945"
---
# <a name="calendar-cell-shape-data-section"></a>[Calendar] セル ([図形データ] セクション)

データ型が Date のとき図形データに使用するカレンダーを指定します。
  
## <a name="remarks"></a>備考

使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | プロペラです。 *名*です。予定表、プロペラします。 *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCustPropsCalendar** <br/> |
   

