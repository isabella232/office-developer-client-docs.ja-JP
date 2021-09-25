---
title: '[Calendar] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
ms.localizationpriority: medium
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: データ型が Date の場合に図形データに使用される予定表を指定します。
ms.openlocfilehash: 81717fd63b49c85a53d66b0e758bfe61c369d7c1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628753"
---
# <a name="calendar-cell-shape-data-section"></a>[Calendar] セル ([Shape Data] セクション)

データ型が Date の場合に図形データに使用される予定表を指定します。
  
## <a name="remarks"></a>注釈

使用できる値は、0 (西暦)、1 (イスラム暦)、2 (ヘブライ太陰暦)、3 (台湾暦)、4 (和暦)、5 (タイ仏暦)、6 (韓国檀紀)、7 (サカ暦)、8 (英語 (音訳))、および 9 (フランス語 (音訳)) です。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Calendar] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Prop。  *name*  .Prop のカレンダー。  *name*  は行名です  <br/> |
   
プログラムから、インデックスによって [Calendar] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCustPropsCalendar** <br/> |
   

