---
title: '[HideText] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
ms.localizationpriority: medium
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: 図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
ms.openlocfilehash: 92e5285d224a7e2c8d43afd38b235cae1e920b1e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574105"
---
# <a name="hidetext-cell-miscellaneous-section"></a>[HideText] セル ([Miscellaneous] セクション)

図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | テキストは表示されず、印刷もされません。  <br/> |
| FALSE  <br/> | テキストは表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または CellsU プロパティを使用したプログラムから名前によって **[HideText]** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | HideText  <br/> |
   
プログラムからインデックスによって [HideText] セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visHideText** <br/> |
   

