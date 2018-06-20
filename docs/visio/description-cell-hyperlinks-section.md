---
title: '[Description] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm230
localization_priority: Normal
ms.assetid: 2f571c65-6b7a-5a3a-c075-3c52d3ab989b
description: ハイパーリンクの説明文を表示します。
ms.openlocfilehash: 567a90b3162c109582c3149c156a994392980577
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805236"
---
# <a name="description-cell-hyperlinks-section"></a>[Description] セル ([Hyperlinks] セクション)

ハイパーリンクの説明文を表示します。 
  
## <a name="remarks"></a>注釈

ハイパーリンクに関するコメント (たとえば  "Link to our pricing Web site." など) は、このセルに格納します。
  
**[ハイパーリンク**] ダイアログ ボックスで、このセルの値を設定することもできます ([**挿入**] タブで**ハイパーリンク**をクリック) します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[説明] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ハイパーリンク  *名*です。説明するハイパーリンク。  *ハイパーリンク行の名前します。*  <br/> |
   
プログラムから、インデックスによって [説明] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
| 行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visHLinkDescription** <br/> |
   

