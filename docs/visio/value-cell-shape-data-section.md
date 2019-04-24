---
title: '[Value] セル ([Shape Data] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1090
localization_priority: Normal
ms.assetid: fd42a6ce-f621-4e9e-aba3-23a1b87a5651
description: '[図形データの定義] ダイアログ ボックスに入力した図形データ項目の値が格納されています。'
ms.openlocfilehash: 40d9e7fdd92ac8fa800a146ea45bbcd002ace87b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355973"
---
# <a name="value-cell-shape-data-section"></a>[Value] セル ([Shape Data] セクション)

[**図形データの定義**] ダイアログ ボックスに入力した図形データ項目の値が格納されています。 
  
## <a name="remarks"></a>解説

このセルに数式を入力しても、[**図形データの定義**] ダイアログ ボックスに入力した値によって上書きされます。式を保護するために GUARD 関数を使用している場合も同様に扱われます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Value] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 提案. *名前*です。値 Prop の値。 *name*には、行の名前を指定します。  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**viscustpropsvalue** <br/> |
   

