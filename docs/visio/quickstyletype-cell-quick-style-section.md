---
title: '[QuickStyleType] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: クイック スタイルの種類を決定 (2 次元、1 次元、またはコネクタ)、図形を継承します。
ms.openlocfilehash: 211074800eee601d2658edbc03bb95d028920e54
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806137"
---
# <a name="quickstyletype-cell-quick-style-section"></a>[QuickStyleType] セル ([クイック スタイル] セクション)

クイック スタイルの種類を決定 (2 次元、1 次元、またはコネクタ)、図形を継承します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |Visio が自動的に選択します。  <br/> |
|1  <br/> |1 次元  <br/> |
|2  <br/> |2 次元  <br/> |
|3  <br/> |コネクタ  <br/> |
   
## <a name="remarks"></a>注釈

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleType** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleType  <br/> |
   
プログラムから、インデックスによって [ **QuickStyleType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleType** <br/> |
   

