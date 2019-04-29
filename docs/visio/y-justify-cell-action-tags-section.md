---
title: '[Y Justify] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026937
localization_priority: Normal
ms.assetid: 27042b62-7623-95d7-7e10-f589d74605c7
description: '[X] セルと [y] セルによって定義された点に対する、アクションタグボタンの y オフセット。'
ms.openlocfilehash: d7a1f5c1feda3624c9f96039e7247c737a91a813
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419983"
---
# <a name="y-justify-cell-action-tags-section"></a>[Y Justify] セル ([Action Tags] セクション)

[X] セルと [y] セルによって定義された点に対する、アクションタグボタンの*y*オフセット。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | 上揃えします (既定値)。  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1   <br/> | 中央揃え  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2   <br/> | 下揃えします。  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>注釈

[x justify] セルと [y justify] セルは、[x] セルと [y] セルで定義されている点に対して、アクションタグボタンが配置される場所を決定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Justify] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | タグ.  *名前*です。SmartTags の位置を指定します。 *name*は、アクションタグ行の名前です。  <br/> |
   
プログラムから、インデックスによって [Y Justify] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visSmartTagYJustify** <br/> |
   

