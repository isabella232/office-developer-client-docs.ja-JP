---
title: '[TagName] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806603"
---
# <a name="tagname-cell-action-tags-section"></a>[TagName] セル ([Action Tags] セクション)

アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>備考

 操作タグ セクションの [tagname] セルとそのアクションのアクション タグを関連付けるには [操作] セクションの [tagname] セルと一緒に動作します。 [操作] セクション内の行も [tagname] セルがあり、このセルと同じ [tagname] セルの値がある行がこのアクションのタグに対して実行するアクションを定義します。 
  
取得する [tagname] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。タグ名、スマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [tagname] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagName** <br/> |
   

