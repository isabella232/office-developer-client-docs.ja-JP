---
title: '[Menu] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: 図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436329"
---
# <a name="menu-cell-actions-section"></a>[Menu] セル ([Actions] セクション)

図形またはページに対するショートカット メニューまたはアクション タグ メニューに表示するメニュー項目の名前を定義します。 
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

メニューのこの項目の上に区切り記号を挿入するには、[BeginGroup] セルを使用します。メニューの下部にコマンドを表示するには、名前の前にパーセント文字 (%) を付けます。
  
別の数式または CellsU プロパティを使用してプログラムから、名前によって **[メニュー** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション。 *name*  .Menuwhere Actions。  *name*  は [アクション] 行の名前です。  <br/> |
   
プログラムから、インデックスによって [Menu] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction**  +  *i* = 0, 1, 2, ...  <br/> |
|セル インデックス:  <br/> |**visActionMenu** <br/> |
   

