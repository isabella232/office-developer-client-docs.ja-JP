---
title: '[Invisible] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
ms.localizationpriority: medium
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: 図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。
ms.openlocfilehash: b0c353f30f4438957334ec79090e3598a84e970e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582604"
---
# <a name="invisible-cell-hyperlinks-section"></a>[Invisible] セル ([Hyperlinks] セクション)

図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |ハイパーリンクは、ショートカット メニューのメニュー項目として表示されません。  <br/> |
|FALSE  <br/> |ハイパーリンクは、ショートカット メニューのメニュー項目として表示されます (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *name*  .ハイパーリンク  *.name が行名*  である場合は非表示  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
|行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visHLinkInvisible** <br/> |
   

