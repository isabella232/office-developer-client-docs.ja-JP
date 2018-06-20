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
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805602"
---
# <a name="invisible-cell-hyperlinks-section"></a>[Invisible] セル ([Hyperlinks] セクション)

図形またはページのショートカット メニューにハイパーリンクがあるかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |ハイパーリンクは、ショートカット メニューのメニュー項目として表示されません。  <br/> |
|FALSE  <br/> |ハイパーリンクは、ショートカット メニューのメニュー項目として表示されます (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって非表示のセルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *名*です。ハイパーリンク *.name*は、行の名前が表示されません。  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
|行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visHLinkInvisible** <br/> |
   

