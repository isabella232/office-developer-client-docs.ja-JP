---
title: '[QuickStyleShadowColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: 0 ~ 7 の整数として、図形の影を使用するテーマの色を決定します。
ms.openlocfilehash: 303a1dfe44960920a6679ea4cc85fb849f8a9cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19806141"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>[QuickStyleShadowColor] セル ([クイック スタイル] セクション)

0 ~ 7 の整数として、図形の影を使用するテーマの色を決定します。
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形の影の色を、[ダーク] テーマの色から継承します。  <br/> |
|1  <br/> |図形の影の色を、[ライト] テーマの色から継承します。  <br/> |
|2  <br/> |図形の影の色を、[アクセント 1] テーマの色から継承します。  <br/> |
|3  <br/> |図形の影の色を、[アクセント 2] テーマの色から継承します。  <br/> |
|4  <br/> |図形の影の色を、[アクセント 3] テーマの色から継承します。  <br/> |
|5  <br/> |図形の影の色を、[アクセント 4] テーマの色から継承します。  <br/> |
|6  <br/> |図形の影の色を、[アクセント 5] テーマの色から継承します。  <br/> |
|7  <br/> |図形の影の色を、[アクセント 6] テーマの色から継承します。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleShadowColor** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleShadowColor  <br/> |
   
プログラムから、インデックスによって [ **QuickStyleShadowColor** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleShadowColor** <br/> |
   

