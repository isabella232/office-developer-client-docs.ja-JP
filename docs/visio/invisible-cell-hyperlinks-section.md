---
title: '[Invisible] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: 図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404632"
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
|セル名:  <br/> |ハイパーリンク *名前*です。非表示ハイパーリンク *。 name*は行名です。  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
|行インデックス:  <br/> |**visRow1stHyperlink** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visHLinkInvisible** <br/> |
   

