---
title: '[LockCrop] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
ms.localizationpriority: medium
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: 別のプログラムのオブジェクトをロックして、[トリミング ツール] を使用したトリミングができないようにします。
ms.openlocfilehash: 0a3224adf6884312c5a722c5b5542a51582a32e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603642"
---
# <a name="lockcrop-cell-protection-section"></a>[LockCrop] セル ([Protection] セクション)

別のプログラムのオブジェクトをロックして、[**トリミング ツール**] を使用したトリミングができないようにします。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形はトリミングできません。  <br/> |
| FALSE  <br/> | 図形はトリミングできます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCrop] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockCrop  <br/> |
   
プログラムから、インデックスによって [LockCrop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockCrop** <br/> |
   

