---
title: '[DisplayLevel] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: 図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408146"
---
# <a name="displaylevel-cell-shape-layout-section"></a>[DisplayLevel] セル ([Shape Layout] セクション)

図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。
  
## <a name="remarks"></a>注釈

Z オーダーは、図面ページの図形の表示順序です。図形の 1 つが他の図形の上に重なっている場合、Z オーダーが大きい図形が Z オーダーの小さい図形の前面に表示されます。 
  
表示レベルは、図形をグループ、つまりバンドに分割します。指定されたバンド内のすべての図形に、下位バンドの図形よりも大きい Z オーダーが設定されます。既定では、ほとんどの図形の表示レベルはゼロ (0) になります。
  
表示レベルの範囲は、-32,767 ～ +32,767 です。表示レベルが同じ図形は 1 つのバンドに結合され、そのバンド内でも Z オーダーを基準にしてランクが付けられます。
  
バンド内の図形の Z オーダーを変更するには、次のコマンドを使用して[前方へ移動]、[後方に送信]、[前面に移動]、および [戻る **] を使用します**。 これらのコマンドが指定したバンドから図形を移動すると、セルが保護されていない限り、Microsoft Visio は図形の DisplayLevel セルに予約値 -32768 を表示します。 その場合、図形を別のバンドに移動することはできません。Visio では、"Shape protection and/layer properties" という警告が表示され、このコマンドが完全に実行されません。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DisplayLevel] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DisplayLevel  <br/> |
   
プログラムから、インデックスによって [DisplayLevel] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLODisplayLevel** <br/> |
   

