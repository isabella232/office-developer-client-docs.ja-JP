---
title: '[BeginGroup] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: このアクションのメニューに区切り記号を挿入するかどうかを示します。
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804802"
---
# <a name="begingroup-cell-actions-section"></a>[BeginGroup] セル ([Actions] セクション)

このアクションのメニューに区切り記号を挿入するかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |区切り記号は、このアクションのメニューに挿入されます。  <br/> |
|FALSE  <br/> |このアクション (デフォルト) のメニューには、区切り文字は挿入されません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって BeginGroup] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。BeginGroup で動作します。 *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [BeginGroup] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionBeginGroup** <br/> |
   

