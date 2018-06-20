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
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805222"
---
# <a name="disabled-cell-actions-section"></a>[Disabled] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |コマンド名を無効 (灰色表示) にします。  <br/> |
|FALSE  <br/> |コマンド名を有効にします (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

取得する、[Disabled] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。無効になっているアクション。 *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [Disabled] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionDisabled** <br/> |
   

