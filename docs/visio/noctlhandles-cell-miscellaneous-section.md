---
title: '[NoCtlHandles] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251319
localization_priority: Normal
ms.assetid: 4345b3e5-f522-e300-307c-4f8992a3ddce
description: 選択した図形のコントロール ハンドルの表示/非表示を切り替えます。
ms.openlocfilehash: 897e4cd97eeab8797f2652285ba395603c41a8e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805915"
---
# <a name="noctlhandles-cell-miscellaneous-section"></a>[NoCtlHandles] セル ([その他] セクション)

選択した図形のコントロール ハンドルの表示/非表示を切り替えます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を選択するときにコントロール ハンドルが表示されません。  <br/> |
| FALSE  <br/> | 図形を選択するときにコントロール ハンドルが表示されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoCtlHandles] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | NoCtlHandles  <br/> |
   
プログラムから、インデックスによる [NoCtlHandles] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowMisc** <br/> |
| セル インデックス:  <br/> |**visNoCtlHandles** <br/> |
   

