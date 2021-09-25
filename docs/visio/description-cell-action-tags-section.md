---
title: '[Description] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
ms.localizationpriority: medium
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。
ms.openlocfilehash: f1e5da6f083d6063403a24df2c980807b441b7b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586559"
---
# <a name="description-cell-action-tags-section"></a>[Description] セル ([Action Tags] セクション)

アクション タグの説明文の文字列を格納します。この説明は、ユーザーがタグの上にポインターを置いたときに、ツール ヒントとして表示されます。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Description] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SmartTags。  *name*  .SmartTags の説明。 *name*  はアクション タグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [Description] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagDescription** <br/> |
   

