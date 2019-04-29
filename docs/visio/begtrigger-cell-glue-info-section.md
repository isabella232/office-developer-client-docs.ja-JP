---
title: '[BegTrigger] セル ([Glue Info] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm100
localization_priority: Normal
ms.assetid: 0b7ffe39-ee6c-71eb-355c-9bb4660260f1
description: アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の始点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
ms.openlocfilehash: b401d349119337016a96b5fffbc26f7be2891864
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437953"
---
# <a name="begtrigger-cell-glue-info-section"></a>[BegTrigger] セル ([Glue Info] セクション)

アプリケーションによって生成されたトリガー数式が格納されています。このトリガー数式によって、1 次元図形の始点を移動するときに別の図形に対する接続を維持するかどうかを指定します。
  
## <a name="remarks"></a>注釈

動的接着を使用して 1 次元図形を別の図形に接着すると、接着先の図形の [EventXFMod] セルを参照する数式がアプリケーションによって生成されます。接着先の図形が変更されると、この図形の [EventXFMod] セルを参照するすべての数式 ([BegTrigger] セルの数式も含む) が再計算されます。1 次元図形の他の数式は [BegTrigger] セルを参照し、必要に応じて 1 次元図形の始点を移動したり、図形を変形します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BegTrigger] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [begtrigger]  <br/> |
   
プログラムから、インデックスによって [BegTrigger] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowGroup** <br/> |
| セル インデックス:  <br/> |**visBegTrigger** <br/> |
   

