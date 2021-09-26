---
title: '[Action] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
ms.localizationpriority: medium
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。
ms.openlocfilehash: 8e1aec829904719f71dde6e87905784e78bd0a1d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608698"
---
# <a name="action-cell-actions-section"></a>[Action] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューのコマンドを選択したときに実行される数式が格納されています。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[Action] セルは、アクションが発生したときにのみ評価されます。数式の入力時には評価されません。
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Action] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | アクション。  *name*  .Action where Actions. *name*  はアクション行の名前です。  <br/> |
   
プログラムから、インデックスによって [Action] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAction** <br/> |
| 行インデックス:  <br/> |**visRowAction**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visActionAction** <br/> |
   

