---
title: '[PageLockDuplicate] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: ページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805958"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>[PageLockDuplicate] セル ([ページのプロパティ] セクション)

ページを複製できるかどうかを、ブール演算型で決定します。
  
|||
|:-----|:-----|
|TRUE  <br/> |ページのショートカット メニューと**Page.Duplicate**オートメーション メソッドの**重複**を両方とも無効ページのです。  <br/> |
|FALSE  <br/> |このページは複製できます。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **PageLockDuplicate** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PageLockDuplicate  <br/> |
   
プログラムから、インデックスによって [ **PageLockDuplicate** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageLockDuplicate** <br/> |
   

