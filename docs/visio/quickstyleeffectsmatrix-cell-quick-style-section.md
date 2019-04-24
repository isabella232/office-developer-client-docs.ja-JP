---
title: '[QuickStyleEffectsMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0332bd3d-626a-4a46-8b69-e887e576ab86
description: アクティブなテーマから図形を継承するクイック スタイル効果を、0 から 6 の整数で決定します。
ms.openlocfilehash: 69541bd7371e8a02838a7ca075d136d8f49c316c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358745"
---
# <a name="quickstyleeffectsmatrix-cell-quick-style-section"></a>[QuickStyleEffectsMatrix] セル ([クイック スタイル] セクション)

アクティブなテーマから図形を継承するクイック スタイル効果を、0 から 6 の整数で決定します。 
  
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの**N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleEffectsMatrix** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [quickstyleeffectsmatrix]  <br/> |
   
プログラムから、インデックスによって [**QuickStyleEffectsMatrix**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleEffectsMatrix** <br/> |
   

