---
title: '[Action] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。
ms.openlocfilehash: 123b05f9a08c4ffa656e08a51f019f888cf83ed4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804750"
---
# <a name="action-cell-actions-section"></a>[Action] セル ([操作] セクション)

ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>備考

[Action] セルは、アクションが発生したときにのみ評価されます。数式の入力時には評価されません。
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Action] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | アクションです。  *名*です。アクション、アクション。 *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Action] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAction** <br/> |
| 行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visActionAction** <br/> |
   

