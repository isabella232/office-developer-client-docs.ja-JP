---
title: '[QuickStyleLineColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: 図形の線で使用するテーマの色を、0 ~ 7 の整数で指定します。
ms.openlocfilehash: 2ebcb23a308ef1c28a87860e9d75bb832e87bba1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623160"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>[QuickStyleLineColor] セル ([クイック スタイル] セクション)

図形の線で使用するテーマの色を、0 ~ 7 の整数で指定します。
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形の線の色は、[ダーク] テーマの色から継承します。  <br/> |
|1  <br/> |図形の線の色は、[ライト] テーマの色から継承します。  <br/> |
|2  <br/> |図形の線の色は、[アクセント 1] テーマの色から継承します  <br/> |
|3  <br/> |図形の線の色は、[アクセント 2] テーマの色から継承します  <br/> |
|4   <br/> |図形の線の色は、[アクセント 3] テーマの色から継承します  <br/> |
|5  <br/> |図形の線の色は、[アクセント 4] テーマの色から継承します  <br/> |
|6   <br/> |図形の線の色は、[アクセント 5] テーマの色から継承します  <br/> |
|7   <br/> |図形の線の色は、[アクセント 6] テーマの色から継承します  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleLineColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleLineColor  <br/> |
   
プログラムから、インデックスによって [**QuickStyleLineColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleLineColor** <br/> |
   

