---
title: '[TagName] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: このアクションに関連付けられているアクション タグの名前を指定します。
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806619"
---
# <a name="tagname-cell-actions-section"></a>[TagName ] セル ([操作] セクション)

このアクションに関連付けられているアクション タグの名前を指定します。
  
> [!NOTE]
> Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。 
  
## <a name="remarks"></a>注釈

[Actions] セクションの [TagName] セルは、[Action Tags] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。 
  
- アクションの行の [tagname] セルが空白の場合、[操作] メニューのタグではなく、ショートカット メニューのアクションが表示されます。
    
- アクション行の [tagname] セルの値には、スマート タグ行の [tagname] セルの値が一致すると、アクションを [アクション] メニューのタグが表示されます。
    
- アクションの [tagname] セルが値を持つタグ行の [tagname] の値に一致しない場合は、そのアクションは任意のアクション タグのメニューまたはショートカット メニューに表示されません。
    
- いくつかのスマート タグ行の [TagName] の値が同じ場合、すべてに同じアクションが表示されます。
    
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクションです。 *名*です。TagNamewhere アクションです。  *アクション行の名前します。*  <br/> |
   
プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visActionTagName** <br/> |
   

