---
title: '[Description] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805223"
---
# <a name="description-cell-action-tags-section"></a>[Description] セル ([操作タグ] セクション)

アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。
  
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。説明するスマート タグ。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagDescription** <br/> |
   

