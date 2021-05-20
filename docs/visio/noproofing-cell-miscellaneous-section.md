---
title: '[NoProofing] セル ([その他] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペルが自動的に修正されるかどうか、および選択した図形にスペル ミスが表示されるかどうかを指定します。 ブール値を取得します。
ms.openlocfilehash: 8d7eebcc349c54db3cd48d6c5fa3c8fa6f4f760e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431254"
---
# <a name="noproofing-cell-miscellaneous-section"></a>[NoProofing] セル ([その他] セクション)

スペルが自動的に修正されるかどうか、および選択した図形にスペル ミスが表示されるかどうかを指定します。 ブール値 **を取得** します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |スペル は自動的に修正されません。選択した図形のスペル ミスは表示されません。  <br/> |
|FALSE  <br/> |スペルが自動的に修正され、選択した図形のスペル ミスが表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

CellsU プロパティを使用して、別の数式またはプログラムから名前によって [NoProofing] セルへの参照を取得するには、次の値を **使用** します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |NoProofing  <br/> |
   
プログラムからインデックスによって [NoProofing] セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visObjNoProofing** <br/> |
   

