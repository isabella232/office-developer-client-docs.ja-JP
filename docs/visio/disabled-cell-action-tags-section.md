---
title: '[Disabled] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: 図面ウィンドウに、アクション タグを表示するかどうかを示します。
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332565"
---
# <a name="disabled-cell-action-tags-section"></a>[Disabled] セル ([Action Tags] セクション)

図面ウィンドウに、アクション タグを表示するかどうかを示します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | アクション タグは無効です。  <br/> |
| FALSE  <br/> | アクション タグは有効です (既定値)。  <br/> |
   
## <a name="remarks"></a>解説

アクション タグを無効にすると、有効にするまで表示されません。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Disabled] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | タグ.  *名前*です。無効 (スマートタグ) *name*は、アクションタグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [Disabled] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagDisabled** <br/> |
   

