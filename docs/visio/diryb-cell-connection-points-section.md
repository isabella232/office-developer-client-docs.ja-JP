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
description: 一致する接続ポイントに必要な配置ベクトルの y コンポーネントを指定します。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332586"
---
# <a name="diry--b-cell-connection-points-section"></a>[DirY / B] セル ([Connection Points] セクション)

一致する接続ポイントに必要な配置ベクトルの*y*コンポーネントを指定します。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数点値が使用されます。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirY / B] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[diry [ *i* ] = <1>、 ** 2、3...  <br/> |
   
プログラムから、インデックスによって [DirY / B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**持つ vissectionconnectionpts** <br/> |
|行インデックス:  <br/> |**visRowConnectionPts** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visCnnctDirY**(非拡張行)          **viscnnctb**(拡張行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

