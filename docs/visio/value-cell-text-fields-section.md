---
title: '[Value] セル ([Text Fields] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1095
localization_priority: Normal
ms.assetid: 3ca662c8-1ce4-89a9-3264-1ba533fcd444
description: フィールドの関数が格納されます。
ms.openlocfilehash: d5a09dd0d59341125db897484f74addff22328de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320203"
---
# <a name="value-cell-text-fields-section"></a>[Value] セル ([Text Fields] セクション)

フィールドの関数が格納されます。
  
## <a name="remarks"></a>解説

このセルの値は、[**フィールド**] ダイアログ ボックスを使用して設定することもできます (このダイアログ ボックスを開くには、[**挿入**] タブの [**テキスト**] グループで、[**フィールド**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Value] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |フィールドの値 [ *i* ]。 *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionTextField** <br/> |
|行インデックス:  <br/> |**visRowField** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visFieldCell** <br/> |
   

