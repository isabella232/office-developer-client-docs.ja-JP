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
description: 図形データの定義] ダイアログ ボックスに入力した図形データ項目の値が含まれています。
ms.openlocfilehash: 5b373149360167585fc5a143ce9458703e219045
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806759"
---
# <a name="value-cell-shape-data-section"></a>[Value] セル ([Shape Data] セクション)

**図形データの定義**] ダイアログ ボックスに入力した図形データ項目の値が含まれています。 
  
## <a name="remarks"></a>備考

このセルに数式を入力は、[**図形データの定義**] ダイアログ ボックスで入力した値によって上書きされます。 GUARD 関数を使用して数式を保護する場合でも同様です。 
  
取得する [値] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | プロペラです。 *名*です。値、プロパティです。 *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionProp** <br/> |
| 行インデックス:  <br/> |**visRowProp** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCustPropsValue** <br/> |
   

