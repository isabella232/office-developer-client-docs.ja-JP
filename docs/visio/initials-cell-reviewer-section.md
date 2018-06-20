---
title: '[Initials] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: 図面の校閲者の頭文字を格納します。
ms.openlocfilehash: 65f0082219c8d6adca55af86c027b2ec5642fb5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805596"
---
# <a name="initials-cell-reviewer-section"></a>[Initials] セル ([Reviewer] セクション)

図面の校閲者の頭文字を格納します。
  
## <a name="remarks"></a>注釈

デフォルト値は、 **Visio のオプション**] ダイアログ ボックスの [**全般**] タブの [**頭文字**] ボックスの [頭文字] (、[**ファイル**] タブをクリックして、**オプション**] をクリックし、し、[**全般**] をクリック) します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [initials] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Reviewer.Initials [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [initials] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visReviewerInitials** <br/> |
   

