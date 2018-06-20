---
title: '[DirY / B] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Y を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 動的コネクタに付いている足の向きにも使用します。 このセルでは浮動小数点値です。
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805217"
---
# <a name="diry--b-cell-connection-points-section"></a>[DirY / B] セル ([Connection Points] セクション)

*Y*を決定に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 動的コネクタに付いている足の向きにも使用します。 このセルでは浮動小数点値です。 
  
## <a name="remarks"></a>備考

[DirY への参照を取得するのには B] セルを別の数式からまたはプログラムからの名前は、 **CellsU**プロパティを使用を使用するとします。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Connections.DirY [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
[DirY への参照を取得するのには B のセルをプログラムから、インデックスによって、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
|行インデックス:  <br/> |**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCnnctDirY**(拡張されていない行)          **visCnnctB**(拡張された行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

