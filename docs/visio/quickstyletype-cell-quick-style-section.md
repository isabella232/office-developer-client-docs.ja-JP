---
title: '[QuickStyleType] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: 図形が継承するクイック スタイル (2 次元、1 次元、またはコネクタ) の種類を決定します。
ms.openlocfilehash: 4dbdb470f3e9bf2db46a47e2efebfd6414256902
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623153"
---
# <a name="quickstyletype-cell-quick-style-section"></a>[QuickStyleType] セル ([クイック スタイル] セクション)

図形が継承するクイック スタイル (2 次元、1 次元、またはコネクタ) の種類を決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |Visio自動的に選択する  <br/> |
|1  <br/> |1 次元  <br/> |
|2  <br/> |2 次元  <br/> |
|3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素 **の N** 属性の値、または CellsU プロパティを使用したプログラムから、名前によって **[QuickStyleType]** セルへの参照を取得するには、次の値を使用します。  
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleType  <br/> |
   
プログラムからインデックスによって **[QuickStyleType]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleType** <br/> |
   

