---
title: '[CtrlAsInput] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1225
localization_priority: Normal
ms.assetid: c6fd0aba-7c33-b77f-207b-ba704b3e0756
description: コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。
ms.openlocfilehash: a87ba7451d73af50de4a110ecdc12b3e23e14d5d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805141"
---
# <a name="ctrlasinput-cell-page-layout-section"></a>[CtrlAsInput] セル ([ページ レイアウト] セクション)

コントロール ハンドルを使用して図形を操作するときに、どの図形を親図形にするかを指定します。このセルの値は、図面ページ上にあるすべての図形の動作に適用されます。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | コントロール ハンドルの接続先になっている図形を親にします。  <br/> |
| FALSE  <br/> | 既定値です。コントロール ハンドルを含んでいる図形を親にします。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [CtrlAsInput] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | CtrlAsInput  <br/> |
   
プログラムから、インデックスによって [CtrlAsInput] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOCtrlAsInput** <br/> |
   

