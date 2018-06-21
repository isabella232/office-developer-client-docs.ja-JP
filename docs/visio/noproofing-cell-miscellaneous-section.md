---
title: NoProofing セル ([その他] セクション)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペル チェックが自動的に修正されたかどうかと、選択した図形のスペル ミスを表示するかどうかを決定します。 ブール値を受け取ります。
ms.openlocfilehash: 6c27e6740b547af83058519de8edd38fc3522b32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19805924"
---
# <a name="noproofing-cell-miscellaneous-section"></a>NoProofing セル ([その他] セクション)

スペル チェックが自動的に修正されたかどうかと、選択した図形のスペル ミスを表示するかどうかを決定します。 **ブール**値を受け取ります。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |スペル チェックが自動的に修正されないと、選択した図形のスペル チェックのエラーは表示されません。  <br/> |
|FALSE  <br/> |スペル チェックが自動的に修正され、選択した図形のスペル チェックのエラーが表示されます。  <br/> |
   
## <a name="remarks"></a>備考

取得する NoProofing] セルへの参照名を別の数式からまたはプログラムでは、 **CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |NoProofing  <br/> |
   
プログラムから、インデックスによって [NoProofing] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visObjNoProofing** <br/> |
   

