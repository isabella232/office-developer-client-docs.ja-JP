---
title: '[LocalizeMerge] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: 図形を図面間でコピーするときにローカライズするかどうかを指定します。
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805730"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>[LocalizeMerge] セル ([Miscellaneous] セクション)

図形を図面間でコピーするときにローカライズするかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | コピー先図面の言語に図形をローカライズします。  <br/> |
| FALSE  <br/> | (既定値) のコピー先の文書の言語に基づく図形のローカライズの操作を行います。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LocalizeMerge] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LocalizeMerge  <br/> |
   
プログラムから、インデックスによって [LocalizeMerge] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visObjLocalizeMerge** <br/> |
   

