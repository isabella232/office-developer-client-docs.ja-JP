---
title: '[DynamicsOff] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251641
localization_priority: Normal
ms.assetid: 055764aa-9681-ffb0-83ce-fdd612fe37af
description: 図面ページ上にある他の図形やコネクタに合わせて、配置可能な図形を移動したり、コネクタを迂回させるかどうかを指定します。
ms.openlocfilehash: 72d65860d1a2ee37efd5287ae3f4baf54bd3addb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805288"
---
# <a name="dynamicsoff-cell-page-layout-section"></a>[DynamicsOff] セル ([ページ レイアウト] セクション)

図面ページ上にある他の図形やコネクタに合わせて、配置可能な図形を移動したり、コネクタを迂回させるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 動的な移動や迂回を無効にします。  <br/> |
| FALSE  <br/> | 動的な移動や迂回を有効にします。  <br/> |
   
## <a name="remarks"></a>備考

動的な移動や迂回を無効にすると、ソリューションのパフォーマンスが向上します。たとえば、ソリューションで図面に配置可能な図形を追加するとき、図形を追加するたびにコネクタの経路変更や、図形の再配置が実行されないようにするには、動的な移動や迂回を無効にします。ソリューションで図形をすべて追加した後に、動的な移動や迂回を再度有効にします。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DynamicsOff] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DynamicsOff  <br/> |
   
プログラムから、インデックスによって [DynamicsOff] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLODynamicsOff** <br/> |
   

