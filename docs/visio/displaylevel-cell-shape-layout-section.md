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
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805213"
---
# <a name="displaylevel-cell-shape-layout-section"></a>[DisplayLevel] セル ([Shape Layout] セクション)

図形の表示レベル バンド (Z オーダー グループ化の相対範囲) を指定します。
  
## <a name="remarks"></a>注釈

Z オーダーは、図面ページの図形の表示順序です。図形の 1 つが他の図形の上に重なっている場合、Z オーダーが大きい図形が Z オーダーの小さい図形の前面に表示されます。 
  
表示レベルは、図形をグループ、つまりバンドに分割します。指定されたバンド内のすべての図形に、下位バンドの図形よりも大きい Z オーダーが設定されます。既定では、ほとんどの図形の表示レベルはゼロ (0) になります。
  
表示レベルの範囲は、-32,767 ～ +32,767 です。表示レベルが同じ図形は 1 つのバンドに結合され、そのバンド内でも Z オーダーを基準にしてランクが付けられます。
  
バンド内の図形の Z オーダーを変更するには、**前面**、**背面****最前面へ移動**、および**最背面へ移動**コマンドを使用します。 場合はこれらのコマンドは、その特定の帯域外の図形を移動、Microsoft Visio は、セルは保護されていない限り、図形のセルに DisplayLevel、-32768 の予約済みの値を表示します。 その場合は、別のバンドでは、図形を移動することはできませんし、警告が表示されます「図形の保護またはレイヤー プロパティは、このコマンドの完全な実行を禁止する」です。 
  
参照を取得する DisplayLevel のセルに名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次の手順を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |DisplayLevel  <br/> |
   
プログラムから、インデックスによって [DisplayLevel] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLODisplayLevel** <br/> |
   

