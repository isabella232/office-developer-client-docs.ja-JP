---
title: '[LockCrop] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: 別のプログラムのオブジェクトをロックして、[トリミング ツール] を使用したトリミングができないようにします。
ms.openlocfilehash: d7f231d5dcb022548477e0817c9d408a8d1b86ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805748"
---
# <a name="lockcrop-cell-protection-section"></a>[LockCrop] セル ([保護] セクション)

別のプログラムのオブジェクトをロックして、[**トリミング ツール**] を使用したトリミングができないようにします。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形はトリミングできません。  <br/> |
| FALSE  <br/> | 図形はトリミングできます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockCrop] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Lockcrop]  <br/> |
   
プログラムから、インデックスによって [LockCrop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockCrop** <br/> |
   

