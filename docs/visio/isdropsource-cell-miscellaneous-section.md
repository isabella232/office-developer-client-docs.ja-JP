---
title: '[IsDropSource] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
localization_priority: Normal
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: 図形をドロップしてグループに追加できるかどうかを指定します。
ms.openlocfilehash: f2edfcb7cf9d21b2ecd97b335b07f30233903d5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805601"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>[IsDropSource] セル ([その他] セクション)

図形をドロップしてグループに追加できるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形をドロップしてグループに追加できます。  <br/> |
|FALSE  <br/> |図形をドロップしてグループに追加できません。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、図形を選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブで [**基本動作**] をクリックし、[**ドロップ時にグループに図形を追加**] チェック ボックスをオンにして設定することもできます。 
  
図形に対してこの動作を有効にする場合、グループに対しても、そのグループにドラッグされた図形を受け入れるように設定する必要があります。このように設定するには、グループを選択して [[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブで [**基本動作**] をクリックし、[**ドロップした図形を受け入れる**] チェック ボックスをオンにします。この値は、[Group Properties] セクションの [IsDropTarget] セルに格納されます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsDropSource] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |IsDropSource  <br/> |
   
プログラムから、インデックスによって [IsDropSource] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visDropSource** <br/> |
   

