---
title: '[PageHeight] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: 図面単位で表した印刷ページの高さを指定します。
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805955"
---
# <a name="pageheight-cell-page-properties-section"></a>[PageHeight] セル ([ページのプロパティ] セクション)

図面単位で表した印刷ページの高さを指定します。
  
## <a name="remarks"></a>注釈

ページの高さは、[**ページ設定**] ダイアログ ボックス ([**デザイン**] タブで [**ページ設定**] 矢印をクリック) の [**ページ サイズ**] タブで設定することも、マウスを使用してページのサイズを手動で変更して設定することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前による [PageHeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |PageHeight  <br/> |
   
プログラムから、インデックスによる [PageHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageHeight** <br/> |
   

