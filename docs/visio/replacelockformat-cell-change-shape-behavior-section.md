---
title: '[ReplaceLockFormat] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。マスター シェイプの [ReplaceLockFormat] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。
ms.openlocfilehash: 2e5f7bb373416ed99f7d4f14cba3aba015243940
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559683"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>[ReplaceLockFormat] セル ([図形の動作の変更] セクション)

マスター シェイプ内の指定したセルの値が、図形の置換操作中に置換される値 (ローカル値を含む) に優先するかどうかを示します。マスター シェイプの [**ReplaceLockFormat**] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |マスター シェイプの [**ReplaceLockFormat**] セルが TRUE (1) に設定されている場合、マスターの書式設定値は、マスターによって置き換えられる図形の対応する値すべてに優先します。  <br/> |
|FALSE  <br/> |マスター シェイプの [**ReplaceLockFormat**] セルが FALSE に設定されている場合、置換後の図形には、置換操作の後、古い図形のローカルの書式設定値が格納されます。  <br/> |
   
## <a name="remarks"></a>注釈

[**ReplaceLockFormat**] セルは、マスター シェイプが、図形の置換操作時に、次のセクション内のローカル書式設定値に優先するかどうかを決定します。 
  
- [**塗りつぶしの書式設定**] セクション 
    
- [**線の書式設定**] セクション 
    
- [**クイック スタイル**] セクション 
    
- [**テーマのプロパティ**] セクション 
    
- [**グラデーションのプロパティ**] セクション 
    
- [**ベベルのプロパティ**] セクション 
    
- [**追加効果のプロパティ**] セクション 
    
- [**線のグラデーションの分岐点**] セクション 
    
- [**塗りつぶしのグラデーションの分岐点**] セクション 
    
別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ReplaceLockFormat**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ReplaceLockFormat  <br/> |
   
プログラムから、インデックスによって [**ReplaceLockFormat**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowReplaceBehaviors** <br/> |
| セル インデックス:  <br/> |**visReplaceLockFormat** <br/> |
   

