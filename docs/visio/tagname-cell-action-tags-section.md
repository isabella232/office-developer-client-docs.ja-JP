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
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332397"
---
# <a name="tagname-cell-action-tags-section"></a>[TagName] セル ([Action Tags] セクション)

アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>解説

 [Action Tags] セクションの [TagName] セルは、[Actions] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。 [Actions] セクションの行には、[tagname] セルがあり、このセルと同じ tagname セル値が指定されている行には、このアクションタグに対して実行するアクションが定義されています。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | タグ.  *名前*です。TagName。 SmartTags *name*は、アクションタグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagName** <br/> |
   

