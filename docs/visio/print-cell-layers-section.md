---
title: '[Print] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: レイヤーに属している図形が印刷可能かどうかを指定します。
ms.openlocfilehash: cd5b2830ba8bd20cb435cdc2bca4bd55fd5a5438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806106"
---
# <a name="print-cell-layers-section"></a>[Print] セル ([Layers] セクション)

レイヤーに属している図形が印刷可能かどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形を印刷できます。  <br/> |
|FALSE  <br/> |図形を印刷できません。  <br/> |
   
## <a name="remarks"></a>注釈

**[レイヤー プロパティ**] ダイアログ ボックスで **[印刷**] オプションを使用してこの値を設定することもできます ([**ホーム**] タブの [**編集**]、[**レイヤー**] をクリックし、[**レイヤー プロパティ**] をクリック) します。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Print] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Layers.Print [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Print] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionLayer** <br/> |
|行インデックス:  <br/> |**visRowLayer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visDocPreviewScope** <br/> |
   

