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
description: Y、X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。
ms.openlocfilehash: 8f8323d1f392654bf118ece2f78890f2a1b860ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806842"
---
# <a name="y-justify-cell-action-tags-section"></a>[Y Justify] セル ([操作タグ] セクション)

*Y* X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 上揃えします (既定値)。  <br/> |**visSmartTagYJustifyTop** <br/> |
| 1  <br/> | 中央揃え  <br/> |**visSmartTagYJustifyMiddle** <br/> |
| 2  <br/> | 下揃えします。  <br/> |**visSmartTagYJustifyBottom** <br/> |
   
## <a name="remarks"></a>注釈

X Justify] および [Y Justify] の各セルは、X と Y のセルで定義されているポイントを基準にして、操作タグ ボタンを配置する場所を決定します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y Justify] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。YJustify、スマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Y Justify] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagYJustify** <br/> |
   

