---
title: '[EndTrigger] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
localization_priority: Normal
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の終点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
ms.openlocfilehash: 9093cca782d9262b2511198ed73f512a75bb8994
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329064"
---
# <a name="endtrigger-cell-glue-info-section"></a>[EndTrigger] セル ([Glue Info] セクション)

アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の終点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
  
## <a name="remarks"></a>解説

動的接着を使用して 1 次元図形を別の図形に接着すると、接着先の図形の [EventXFMod] セルを参照する数式が Visio によって生成されます。接着先の図形が変更されると、この図形の [EventXFMod] セルを参照するすべての数式 ([EndTrigger] セルの数式も含む) が再計算されます。1 次元図形の他の数式は [EndTrigger] セルを参照し、必要に応じて 1 次元図形の終点を移動したり、図形を変形します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EndTrigger] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [endtrigger]  <br/> |
   
プログラムから、インデックスによって [EndTrigger] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visendtrigger** <br/> |
   

