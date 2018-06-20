---
title: '[D] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm205
localization_priority: Normal
ms.assetid: 28b18e8d-fecf-a798-813e-c1a310002244
description: 数式を入力またはテストするために使用できる、スクラッチ セルです。
ms.openlocfilehash: 21c81c7a0a64c3016d8cff3b33d83ce785dc24eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805150"
---
# <a name="d-cell-connection-points-section"></a>[D] セル ([Connection Points] セクション)

数式を入力またはテストするために使用できる、スクラッチ セルです。
  
## <a name="remarks"></a>備考

[D] セルにアクセスするには、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [D] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Connections.D [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [D] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visCnnctD** <br/> |
   

