---
title: '[Type / C] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251723
localization_priority: Normal
ms.assetid: 2264d026-2041-3855-2b23-553ce67ae69d
description: 接続ポイントの種類を指定します。
ms.openlocfilehash: a73554d9f3a3bce6a039689d2c0b192a1c5b69aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415237"
---
# <a name="type--c-cell-connection-points-section"></a>[Type / C] セル ([Connection Points] セクション)

接続ポイントの種類を指定します。
  
|**値**|**型**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |Inward  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |外向き  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |内側外側 &amp;  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>注釈

接続ポイントの種類は、[**コネクタ**] ツールを選択し、図形を選択してから、接続ポイントを右クリックして設定することもできます。この操作は、[開発](run-in-developer-mode-display-the-developer-tab.md)モードで実行する必要があります。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Type / C] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Connections.Type[  *i*  ] where i =  *<*  1> 2, 3...  <br/> |
   
プログラムから、インデックスによって [Type / C] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
|行インデックス:  <br/> |**visRowConnectionPts**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCnnctType** (拡張されていない行) **visCnnctC** (拡張行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

