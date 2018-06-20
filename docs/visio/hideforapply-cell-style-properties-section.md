---
title: '[HideForApply] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Microsoft Visio ユーザー インターフェイスのスタイルを表示する場所を決定します。
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805541"
---
# <a name="hideforapply-cell-style-properties-section"></a>[HideForApply] セル ([Style Properties] セクション)

Microsoft Visio ユーザー インターフェイスのスタイルを表示する場所を決定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | **ドローイング エクスプ ローラー**でのみスタイルを表示します。  <br/> |
| FALSE  <br/> | **ドローイング エクスプ ローラー]** でスタイルを表示します。  <br/> |
   
## <a name="remarks"></a>備考

表示されていないスタイルに基づいて新しいスタイルを作成する場合は、この属性は継承されません。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[HideForApply] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | HideForApply  <br/> |
   
プログラムから、インデックスによって [HideForApply] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowStyle** <br/> |
| セル インデックス:  <br/> |**visStyleHidden** <br/> |
   

