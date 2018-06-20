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
ms.openlocfilehash: 12c953a160ab99aad007e9b2bb9089d651aee553
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806708"
---
# <a name="type--c-cell-connection-points-section"></a>[Type / C] セル ([Connection Points] セクション)

接続ポイントの種類を指定します。
  
|**値**|**型**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |内向き  <br/> |**visCnnctTypeInward** <br/> |
|1  <br/> |外向き  <br/> |**visCnnctTypeOutward** <br/> |
|2  <br/> |内側&amp;外向き  <br/> |**visCnnctTypeInwardOutward** <br/> |
   
## <a name="remarks"></a>備考

**コネクタ**ツールを選択する、図形を選択し、接続ポイントを右クリックし、接続ポイントの種類を設定することもできます。 これを行うには、[開発](run-in-developer-mode-display-the-developer-tab.md)モードで実行する必要があります。 
  
型への参照を取得するのには C は、 **CellsU**プロパティを使用して、別の数式からまたはプログラムの名前でセルとします。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Connections.Type [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
型への参照を取得するのには C] セルをプログラムから、インデックスによって、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
|行インデックス:  <br/> |**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visCnnctType**(拡張されていない行)**visCnnctC**(拡張された行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

