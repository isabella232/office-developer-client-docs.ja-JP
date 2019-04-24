---
title: '[Disabled] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332579"
---
# <a name="disabled-cell-actions-section"></a>[Disabled] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |コマンド名を無効 (灰色表示) にします。  <br/> |
|FALSE  <br/> |コマンド名を有効にします (既定値)。  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Disabled] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |アクション. *名前*です。無効にするアクション。 *name*は、Actions 行の名前です。  <br/> |
   
プログラムから、インデックスによって [Disabled] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* = ** 0、1、2...  <br/> |
|セル インデックス:  <br/> |**visActionDisabled** <br/> |
   

