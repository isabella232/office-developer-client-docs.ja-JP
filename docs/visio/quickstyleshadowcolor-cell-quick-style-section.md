---
title: '[QuickStyleShadowColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: 図形の影で使用するテーマの色を、0 ~ 7 の整数で指定します。
ms.openlocfilehash: 5578a8da853020234338119f147dfc610610f7f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618617"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>[QuickStyleShadowColor] セル ([クイック スタイル] セクション)

図形の影で使用するテーマの色を、0 ~ 7 の整数で指定します。
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形の影の色を、[ダーク] テーマの色から継承します。  <br/> |
|1  <br/> |図形の影の色を、[ライト] テーマの色から継承します。  <br/> |
|2  <br/> |図形の影の色を、[アクセント 1] テーマの色から継承します。  <br/> |
|3  <br/> |図形の影の色を、[アクセント 2] テーマの色から継承します。  <br/> |
|4   <br/> |図形の影の色を、[アクセント 3] テーマの色から継承します。  <br/> |
|5  <br/> |図形の影の色を、[アクセント 4] テーマの色から継承します。  <br/> |
|6   <br/> |図形の影の色を、[アクセント 5] テーマの色から継承します。  <br/> |
|7   <br/> |図形の影の色を、[アクセント 6] テーマの色から継承します。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleShadowColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleShadowColor  <br/> |
   
プログラムから、インデックスによって[**QuickStyleShadowColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleShadowColor** <br/> |
   

