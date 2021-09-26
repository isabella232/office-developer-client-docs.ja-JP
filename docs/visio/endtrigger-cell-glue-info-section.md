---
title: '[EndTrigger] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251331
ms.localizationpriority: medium
ms.assetid: 8dc6515b-66ab-f1ac-18fd-820209f90991
description: アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の終点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
ms.openlocfilehash: 395a53d792b8a9cad336c816be255d2ee4d15aca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619093"
---
# <a name="endtrigger-cell-glue-info-section"></a>[EndTrigger] セル ([Glue Info] セクション)

アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の終点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
  
## <a name="remarks"></a>注釈

動的接着を使用して 1 次元図形を別の図形に接着すると、接着先の図形の [EventXFMod] セルを参照する数式が Visio によって生成されます。接着先の図形が変更されると、この図形の [EventXFMod] セルを参照するすべての数式 ([EndTrigger] セルの数式も含む) が再計算されます。1 次元図形の他の数式は [EndTrigger] セルを参照し、必要に応じて 1 次元図形の終点を移動したり、図形を変形します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EndTrigger] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | EndTrigger  <br/> |
   
プログラムから、インデックスによって [EndTrigger] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visEndTrigger** <br/> |
   

