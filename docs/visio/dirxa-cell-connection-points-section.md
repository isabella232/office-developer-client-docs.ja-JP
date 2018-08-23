---
title: '[DirX / A] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: X を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 DirX/動的コネクタに付いている足の方向を設定するセルを使用しても。 このセルでは浮動小数点値です。
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805246"
---
# <a name="dirx--a-cell-connection-points-section"></a>[DirX / A] セル ([接続ポイント] セクション)

*X*を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 DirX/動的コネクタに付いている足の方向を設定するセルを使用しても。 このセルでは浮動小数点値です。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirX / A] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Connections.DirX [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [DirX / A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2  <br/> |
| セル インデックス:  <br/> |**visCnnctDirX**(拡張されていない行)          **visCnnctA**(拡張された行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

