---
title: '[ButtonFace] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60025
localization_priority: Normal
ms.assetid: cf15b879-a47e-a5a5-bfdd-1d7ea423742f
description: ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
ms.openlocfilehash: 7ee9c4e7e857acb34ce75429aa0aaf679320b0e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407376"
---
# <a name="buttonface-cell-actions-section"></a>[ButtonFace] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューで、項目の横に表示されるアイコンを指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[ButtonFace] セルに含まれる文字列は Microsoft Office のボタン イメージの ID を表します。値ゼロ (0) または空白は、アイコンが表示されないことを示します。 
  
[ButtonFace] セルに使用される ID は、 **CommandBarButton ** オブジェクトの  **FaceID ** プロパティで使用される ID と同じです。 これらの id の詳細については、MSDN の「コマンドバーボタンイメージを使用する」を検索してください。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ButtonFace] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |**アクション**。  *名前*です。 **アクション**を実行する**buttonface** 。  *name*は、actions 行の名前です。  <br/> |
   
プログラムから、インデックスによって [ButtonFace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* = **** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visActionButtonFace** <br/> |
   

