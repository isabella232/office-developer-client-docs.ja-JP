---
title: '[TagName] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
ms.localizationpriority: medium
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
ms.openlocfilehash: 09bd43f69e1adb757ab71e34b232f79affa10e2d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622754"
---
# <a name="tagname-cell-action-tags-section"></a>[TagName] セル ([Action Tags] セクション)

アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

 [Action Tags] セクションの [TagName] セルは、[Actions] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。 [アクション] セクションの行には [TagName] セルも含まれます。また、このセルと同じ TagName セル値を持つ行は、このアクション タグに対して実行するアクションを定義します。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SmartTags。  *name*  .SmartTags の TagName。 *name*  はアクション タグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagName** <br/> |
   

