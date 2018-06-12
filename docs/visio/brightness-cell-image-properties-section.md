---
title: '[Brightness] セル ([Image Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251608
localization_priority: Normal
ms.assetid: 5bb1cc81-f3fd-a835-1449-233dbd1a62b6
description: ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。
ms.openlocfilehash: 688a6cacfa9100ad116b9bf06926194c24712219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804917"
---
# <a name="brightness-cell-image-properties-section"></a>[Brightness] セル ([Image Properties] セクション)

ビットマップ イメージの明るさを調整します。0 ～ 49% の範囲で値を入力するとイメージの輝度が下がります。51 ～ 100% の範囲で値を入力するとイメージの輝度が上がります。既定値は 50% です。
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[明るさ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Brightness  <br/> |
   
プログラムから、インデックスによって [明るさ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowImage** <br/> |
| セル インデックス:  <br/> |**visImageBrightness** <br/> |
   

