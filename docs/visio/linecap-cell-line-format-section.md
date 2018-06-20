---
title: '[LineCap] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251231
localization_priority: Normal
ms.assetid: 3519216b-b6cf-2e8c-e20f-adfa373c9028
description: 線の端点を丸、四角形、または拡張のどれにするかを指定します。
ms.openlocfilehash: 1bd427801e6d95ce6167fa9681da2c567307f072
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805703"
---
# <a name="linecap-cell-line-format-section"></a>[LineCap] セル ([Line Format] セクション)

線の端点を丸、四角形、または拡張のどれにするかを指定します。
  
|**値**|**線の終点のスタイル**|
|:-----|:-----|
|0  <br/> |丸  <br/> |
|1  <br/> |四角形  <br/> |
|2  <br/> |拡張  <br/> |
   
## <a name="remarks"></a>注釈

**線**] ダイアログ ボックスで、このセルの値を設定することもできます ([**ホーム**] タブの [**図形**] グループで、[**行**] をクリックして、**矢印**] をポイントし、**複数の矢印**をクリックして)。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [linecap] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Linecap]  <br/> |
   
プログラムから、インデックスによって [linecap] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLineEndCap** <br/> |
   

