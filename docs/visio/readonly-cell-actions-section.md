---
title: '[ReadOnly] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806145"
---
# <a name="readonly-cell-actions-section"></a>[ReadOnly] セル ([Actions] セクション)

ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |アクションはメニューに表示されますが、読み取り専用です。  <br/> |
|FALSE  <br/> |アクションはメニューに表示され、選択できます (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

読み取り専用操作では、アクションのタグやショートカット メニューに表示されますがそれを選択することはできません。 淡色表示されますが、ラベルのように、色付きの背景に表示されます。 メニュー項目が淡色表示にするには、無効なセルを使用します。 
  
参照を取得する読み取り専用のセルに名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。ReadOnlywhere アクションです。  *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [ReadOnly] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionReadOnly** <br/> |
   

