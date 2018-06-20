---
title: '[NewWindow] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805919"
---
# <a name="newwindow-cell-hyperlinks-section"></a>[NewWindow] セル ([Hyperlinks] セクション)

ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | リンクされたページ、図面、または Web サイトを新しいウィンドウで開きます。  <br/> |
| FALSE  <br/> | 既定値です。ハイパーリンク用に新しいウィンドウを開きません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムからは、名前によって、[NewWindow] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名*です。NewWindow いるハイパーリンク。  *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [NewWindow] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0、1、2、.  <br/> |
| セル インデックス:  <br/> |**visHLinkNewWin** <br/> |
   

