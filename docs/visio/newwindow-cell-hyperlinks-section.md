---
title: '[NewWindow] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
ms.localizationpriority: medium
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
ms.openlocfilehash: b77da67f595ff25e235c2b2b01f292fe5b31013e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563001"
---
# <a name="newwindow-cell-hyperlinks-section"></a>[NewWindow] セル ([Hyperlinks] セクション)

ハイパーリンクを新しいウィンドウで開くかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | リンクされたページ、ドキュメント、または Web サイトを新しいウィンドウで開きます。  <br/> |
| FALSE  <br/> | 既定値です。ハイパーリンク用に新しいウィンドウを開きません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NewWindow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ハイパーリンク  *Name*  .NewWindow where Hyperlink.  *名前*  は行名です  <br/> |
   
プログラムから、インデックスによって [NewWindow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink**  +  *i* *=* 0, 1, 2, ...  <br/> |
| セル インデックス:  <br/> |**visHLinkNewWin** <br/> |
   

