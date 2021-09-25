---
title: '[LineCap] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
ms.localizationpriority: medium
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: 線の端点を丸、四角形、または拡張のどれにするかを指定します。
ms.openlocfilehash: b062ff673d561a7c328b361fea8da0c4f67024c0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615901"
---
# <a name="linecap-cell-line-format-section"></a>[LineCap] セル ([Line Format] セクション)

線の端点を丸、四角形、または拡張のどれにするかを指定します。
  
|**値**|**線の端点の形**|
|:-----|:-----|
|0  <br/> |四捨五入  <br/> |
|1  <br/> |四角  <br/> |
|2  <br/> |拡張  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、[**線**] ダイアログ ボックスで設定することもできます (このダイアログ ボックスを開くには、[**ホーム**] タブの [**図形**] グループで、[**線**] をクリックし、[**矢印**] をポイントして、[**その他の矢印**] をクリックします)。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LineCap] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LineCap  <br/> |
   
プログラムから、インデックスによって [LineCap] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineEndCap** <br/> |
   

