---
title: '[SketchAmount] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806502"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>[SketchAmount] セル ([追加効果のプロパティ] セクション)

スケッチ効果に対するゆがみの量を、0 から 25 の整数で決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |図形には、適用されるスケッチ効果はありません。  <br/> |
|1-25  <br/> |図形には、スケッチのゆがみが適用されています。1 の値ではゆがみがもっとも大きく、25 ではもっとも小さくなります。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **SketchAmount** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SketchAmount  <br/> |
   
プログラムから、インデックスによって [ **SketchAmount** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visSketchAmount** <br/> |
   

