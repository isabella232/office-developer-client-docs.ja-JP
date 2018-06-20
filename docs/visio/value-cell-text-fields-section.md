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
ms.openlocfilehash: 9bce4cbb1b3955f749cefa18130c6b01fe61244e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806749"
---
# <a name="value-cell-text-fields-section"></a>[Value] セル ([Text Fields] セクション)

フィールドの関数が格納されます。
  
## <a name="remarks"></a>注釈

**フィールド**] ダイアログ ボックスを使用してこのセルの値を設定することができます ([**挿入**] タブの [**テキスト**] で、[**フィールド**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [値] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Fields.Value [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Value] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionTextField** <br/> |
|行インデックス:  <br/> |**visRowField** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visFieldCell** <br/> |
   

