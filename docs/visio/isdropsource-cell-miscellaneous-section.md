---
title: '[IsDropSource] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm490
ms.localizationpriority: medium
ms.assetid: 3b20e6ef-f1ac-5bb0-5ac3-4df3ae5e9bf9
description: 図形をドロップしてグループに追加できるかどうかを指定します。
ms.openlocfilehash: c56b456f76f0f211648caf183e88380a23942dac
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628053"
---
# <a name="isdropsource-cell-miscellaneous-section"></a>[IsDropSource] セル ([Miscellaneous] セクション)

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
   

