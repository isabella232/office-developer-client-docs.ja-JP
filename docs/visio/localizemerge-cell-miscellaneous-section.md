---
title: '[LocalizeMerge] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
ms.localizationpriority: medium
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: 図形を図面間でコピーするときにローカライズするかどうかを指定します。
ms.openlocfilehash: 9f2e3e689814891f1a8cd4c69d7656fe6d1b22c9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615880"
---
# <a name="localizemerge-cell-miscellaneous-section"></a>[LocalizeMerge] セル ([Miscellaneous] セクション)

図形を図面間でコピーするときにローカライズするかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | コピー先図面の言語に図形をローカライズします。  <br/> |
| FALSE  <br/> | 変換先の文書の言語 (既定) に基づいて図形をローカライズしない。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LocalizeMerge] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LocalizeMerge  <br/> |
   
プログラムから、インデックスによって [LocalizeMerge] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visObjLocalizeMerge** <br/> |
   

