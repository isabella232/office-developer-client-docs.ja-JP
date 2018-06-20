---
title: '[LineGradientDir] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: 線のグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805712"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a>[LineGradientDir] セル ([グラデーションのプロパティ] セクション)

線のグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。 
  
> [!NOTE]
> 線形グラデーションは、グラデーション ( **LineGradientDir**セルによって決まります)、その他の角度の値を受け取るだけです。 他のすべてのグラデーションの方向には、列挙値が事前設定されます。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |線形グラデーションです。 **LineGradientAngle**セルでは、グラデーションの方向を決定します。  <br/> |
|1-7  <br/> |放射状のグラデーション。グラデーションは円の中央から外側に向かって拡張されます。  <br/> |
|8-12  <br/> |角形のグラデーション。グラデーションは、角形のフェードを使用して原点から矢印線として拡張されます。  <br/> |
|13  <br/> |パスのグラデーション。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LineGradientDir** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LineGradientDir  <br/> |
   
プログラムから、インデックスによって [ **LineGradientDir** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visLineGradientDir** <br/> |
   

