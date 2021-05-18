---
title: '[X Justify] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: X セルと Y セルで定義されたポイントを基準にしたアクション タグ ボタンの x -offset。
ms.openlocfilehash: f8542d2f3a22b12794d999323d202d7a5bece20b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414124"
---
# <a name="x-justify-cell-action-tags-section"></a>[X Justify] セル ([Action Tags] セクション)

X  *セル*  と Y セルで定義されたポイントを基準にしたアクション タグ ボタンの x -offset。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 左揃えします (既定値)。  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | 中央揃え  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | 右揃えします。  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>注釈

[X Justify] セルと [Y Justify] セルは、アクション タグ ボタンが X セルと Y セルで定義されているポイントとの関係で配置される場所を決定します。 
  
別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [X Justify] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | SmartTags。  *name*  .XJustify where SmartTags. *name*  はアクション タグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [X Justify] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagXJustify** <br/> |
   

