---
title: '[Invisible] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805593"
---
# <a name="invisible-cell-actions-section"></a>[Invisible] セル ([Actions] セクション)

アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |アクションはメニューに表示されません。  <br/> |
|FALSE  <br/> |アクションはメニューに表示されます (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

参照を取得する非表示のセルに名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。Invisiblewhere アクションです。  *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Invisible] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionInvisible** <br/> |
   

