---
title: '[QuickStyleLineColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: 0 ~ 7 の整数として、図形の線を使用するテーマの色を決定します。
ms.openlocfilehash: 2a660472998ade8148e8b70a3c6e4fc5fb3f4820
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806153"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>[QuickStyleLineColor] セル ([クイック スタイル] セクション)

0 ~ 7 の整数として、図形の線を使用するテーマの色を決定します。
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形の線の色は、[ダーク] テーマの色から継承します。  <br/> |
|1  <br/> |図形の線の色は、[ライト] テーマの色から継承します。  <br/> |
|2  <br/> |図形の線の色は、[アクセント 1] テーマの色から継承します  <br/> |
|3  <br/> |図形の線の色は、[アクセント 2] テーマの色から継承します  <br/> |
|4  <br/> |図形の線の色は、[アクセント 3] テーマの色から継承します  <br/> |
|5  <br/> |図形の線の色は、[アクセント 4] テーマの色から継承します  <br/> |
|6  <br/> |図形の線の色は、[アクセント 5] テーマの色から継承します  <br/> |
|7  <br/> |図形の線の色は、[アクセント 6] テーマの色から継承します  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleLineColor** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleLineColor  <br/> |
   
プログラムから、インデックスによって [ **QuickStyleLineColor** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleLineColor** <br/> |
   

