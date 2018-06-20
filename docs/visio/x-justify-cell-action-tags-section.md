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
description: X、X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806812"
---
# <a name="x-justify-cell-action-tags-section"></a>[X Justify] セル ([Action Tags] セクション)

*X*の X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 左揃えします (既定値)。  <br/> |**visSmartTagXJustifyLeft** <br/> |
| 1  <br/> | 中央揃え  <br/> |**visSmartTagXJustifyCenter** <br/> |
| 2  <br/> | 右揃えします。  <br/> |**visSmartTagXJustifyRight** <br/> |
   
## <a name="remarks"></a>備考

X Justify] および [Y Justify] の各セルは、X と Y のセルで定義されているポイントを基準にして、操作タグ ボタンを配置する場所を決定します。 
  
取得する、[X Justify] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | スマート タグです。  *名*です。XJustify、スマート タグです。 *タグのアクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [X Justify] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionSmartTag** <br/> |
| 行インデックス:  <br/> |**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visSmartTagXJustify** <br/> |
   

