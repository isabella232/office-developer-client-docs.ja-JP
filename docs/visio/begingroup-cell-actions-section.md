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
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361034"
---
# <a name="begingroup-cell-actions-section"></a>[BeginGroup] セル ([Actions] セクション)

このアクションのメニューに区切り記号を挿入するかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |このアクションのメニューに区切り記号を挿入します。  <br/> |
|FALSE  <br/> |このアクションのメニューに区切り記号を挿入しません (既定値)。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginGroup] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション. *名前*です。アクションを実行する begingroup。 *name* には [Actions] 行の名前を指定  <br/> |
   
プログラムから、インデックスによって [BeginGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visActionBeginGroup** <br/> |
   

