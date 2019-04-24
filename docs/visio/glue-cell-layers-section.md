---
title: '[Glue] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: レイヤーに属している図形が接着可能かどうかを指定します。
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332810"
---
# <a name="glue-cell-layers-section"></a>[Glue] セル ([Layers] セクション)

レイヤーに属している図形が接着可能かどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |接着できます。  <br/> |
|FALSE  <br/> |接着できません。  <br/> |
   
## <a name="remarks"></a>解説

このセルは、[**レイヤープロパティ**] ダイアログボックス ([**ホーム**] タブの [**編集**] グループで、[**レイヤー**] をクリックし、[**レイヤープロパティ**] をクリック) の [**接着**] オプションに対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Glue] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |レイヤー. グルー [ *i* ] = ** <1>, 2, 3...  <br/> |
   
プログラムから、インデックスによって [Glue] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visLayerGlue** <br/> |
   

