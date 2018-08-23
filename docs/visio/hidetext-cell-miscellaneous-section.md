---
title: '[HideText] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: 図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805536"
---
# <a name="hidetext-cell-miscellaneous-section"></a>[HideText] セル ([その他] セクション)

図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | テキストは表示されず、印刷もされません。  <br/> |
| FALSE  <br/> | テキストは表示されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[HideText] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | HideText  <br/> |
   
プログラムから、インデックスによって [HideText] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visHideText** <br/> |
   

