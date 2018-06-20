---
title: '[LinePattern] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm560
localization_priority: Normal
ms.assetid: a416762b-7294-c99f-d9f1-332c3ed35dff
description: 図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。
ms.openlocfilehash: cccc6028de21299942e62c53aba48622baa95f98
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805708"
---
# <a name="linepattern-cell-line-format-section"></a>[LinePattern] セル ([Line Format] セクション)

図形の線の種類を指定します。[LinePattern] セルには、線の種類のコレクション内でインデックスとなっている数字を入力します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |線の種類なし  <br/> |
|1  <br/> |実線  <br/> |
|2-23  <br/> |さまざまな線の種類  <br/> |
   
## <a name="remarks"></a>注釈

線のパターンのコレクションを表示するには [**線**] ダイアログ ボックス ([**ホーム**] タブの [**図形**] グループで、**行**、**ダッシュ**をし、**他の線**] をクリック) します。
  
ユーザー設定の線のパターンを指定するには、このセルで USE 関数を使用します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LinePattern] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LinePattern  <br/> |
   
プログラムから、インデックスによって [LinePattern] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLine** <br/> |
|セル インデックス:  <br/> |**visLinePattern** <br/> |
   

