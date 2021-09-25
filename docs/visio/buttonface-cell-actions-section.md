---
title: '[ButtonFace] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
ms.localizationpriority: medium
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
ms.openlocfilehash: 96610ad6e1add550ab6ed940b7dc2ccbfb8373da
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608614"
---
# <a name="buttonface-cell-actions-section"></a>[ButtonFace] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[ButtonFace] セルに含まれる文字列は Microsoft Office のボタン イメージの ID を表します。値ゼロ (0) または空白は、アイコンが表示されないことを示します。 
  
[ButtonFace] セルに使用される ID は、 **CommandBarButton** オブジェクトの  **FaceID** プロパティで使用される ID と同じです。 これらの ID の詳細については、MSDN で "コマンド バー ボタンイメージを操作する" を検索します。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |**アクション**。  *name*  . **ButtonFace**         where **Actions**.  *name*  はアクション行の名前です。  <br/> |
   
プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction**  +  *i* **=** 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visActionButtonFace** <br/> |
   

