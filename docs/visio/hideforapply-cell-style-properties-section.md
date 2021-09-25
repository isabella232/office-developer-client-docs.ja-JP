---
title: '[HideForApply] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
ms.localizationpriority: medium
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Microsoft ユーザー インターフェイスでスタイルを表示するVisioします。
ms.openlocfilehash: 18750f8191d468483b63f7e076ada1b4cd2072f7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570492"
---
# <a name="hideforapply-cell-style-properties-section"></a>[HideForApply] セル ([Style Properties] セクション)

Microsoft ユーザー インターフェイスでスタイルを表示するVisioします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | [**ドローイング エクスプローラー**] だけにスタイルを表示します。  <br/> |
| FALSE  <br/> | [**ドローイング エクスプローラー**] にスタイルを表示します。  <br/> |
   
## <a name="remarks"></a>注釈

表示されていないスタイルに基づいて新しいスタイルを作成する場合は、この属性は継承されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [HideForApply] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | HideForApply  <br/> |
   
プログラムから、インデックスによって [HideForApply] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowStyle** <br/> |
| セル インデックス:  <br/> |**visStyleHidden** <br/> |
   

