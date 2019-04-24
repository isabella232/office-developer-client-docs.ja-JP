---
title: '[Controls] 行 ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
localization_priority: Normal
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: 図形に定義されている各コントロールハンドルの x 座標と y 座標、および動作を定義するセルを格納します。 図形には、各コントロールハンドルに対して1つの Controls 行が含まれます。
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282958"
---
# <a name="controls-row-controls-section"></a>[Controls] 行 ([Controls] セクション)

図形に定義されている各コントロールハンドルの*x*座標と*y*座標、および動作を定義するセルを格納します。 図形には、各コントロールハンドルに対して1つの Controls 行が含まれます。 
  
[Controls] 行の名前は Controls. 次のセルに*名前*とが含まれます。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |図形のコントロールハンドルの位置を示す*x*座標を、ローカル座標で表します。  <br/> |
|[y](y-cell-controls-section.md) <br/> |図形のコントロールハンドルの位置を示す*y*座標を、ローカル座標で表します。  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |コントロールハンドルのアンカーポイントの*x*座標を、ローカル座標で表します。  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |コントロールハンドルのアンカーポイントの*y*座標を、ローカル座標で表します。  <br/> |
|[X Behavior](x-behavior-cell-controls-section.md) <br/> |ハンドルを移動したときにコントロールハンドルの*x*座標が示す動作の種類を制御します。  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |ハンドルを移動したときにコントロールハンドルの*y*座標が示す動作の種類を制御します。  <br/> |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |コントロール ハンドルを他の図形に接着できるかを指定します。  <br/> |
|[部](tip-cell-controls-section.md) <br/> |ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを重ねたときに表示されます。  <br/> |
   
## <a name="remarks"></a>解説

 必要に応じて [Controls.  必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。 既存の [Controls] セクションにコントロール ハンドルを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルを行名で参照できます。これは、シェイプシートウィンドウに赤いテキストで表示されます。 コントロールにわかりやすい名前を割り当てる。 [*名前*] 行をクリックしてから、「 *custom* 」と入力します。たとえば、行名のコントロールを作成します。 その後、コントロールを使用して [x] セルを参照することができます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

