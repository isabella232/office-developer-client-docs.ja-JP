---
title: '[noproofing] セル ([その他] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペルを自動的に修正するかどうか、および選択した図形のスペルミスを表示するかどうかを指定します。 ブール値を受け取ります。
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431254"
---
# <a name="noproofing-cell-miscellaneous-section"></a>[noproofing] セル ([その他] セクション)

スペルを自動的に修正するかどうか、および選択した図形のスペルミスを表示するかどうかを指定します。 **ブール**値を受け取ります。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |スペルチェックは自動的には修正されず、選択した図形のスペルミスは表示されません。  <br/> |
|FALSE  <br/> |スペルチェックは自動的に修正され、選択した図形のスペルミスが表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または**CellsU**プロパティを使用してプログラムから、名前によって [noproofing] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |NoProofing  <br/> |
   
プログラムから、インデックスによって [noproofing] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visobjnoproofing** <br/> |
   

