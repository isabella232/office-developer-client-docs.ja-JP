---
title: '[NoObjHandles] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm730
localization_priority: Normal
ms.assetid: 8e1c8c8f-4ed0-0f53-f93f-3a264edc02bd
description: 選択した図形の選択ハンドルの表示/非表示を切り替えます。
ms.openlocfilehash: 8f812c2087870529cb65aa2e7d705171a5d4ca32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805947"
---
# <a name="noobjhandles-cell-miscellaneous-section"></a>[NoObjHandles] セル ([その他] セクション)

選択した図形の選択ハンドルの表示/非表示を切り替えます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を選択するときに選択ハンドルが表示されません。  <br/> |
| FALSE  <br/> | 図形を選択するときに選択ハンドルが表示されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoObjHandles] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | NoObjHandles  <br/> |
   
プログラムから、インデックスによって [NoObjHandles] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNoObjHandles** <br/> |
   

