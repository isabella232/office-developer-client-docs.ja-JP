---
title: '[NoProofing] セル ([その他] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 668f993c-b4d1-4762-9801-c578b17fdafd
description: スペルが自動的に修正されるかどうか、および選択した図形にスペル ミスが表示されるかどうかを指定します。 ブール値を取得します。
ms.openlocfilehash: 6e4ffc00e9d45c808655363619a5331030cb84a2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573832"
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
   

