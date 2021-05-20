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
description: 図形に対して定義された各コントロール ハンドルの x 座標と y 座標と動作を定義するセルが含まれる。 図形には、コントロール ハンドルごとに 1 つの Controls 行が含まれます。
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438191"
---
# <a name="controls-row-controls-section"></a>[Controls] 行 ([Controls] セクション)

図形に対して定義された各コントロール ハンドルの  *x*  座標と  *y*  座標と動作を定義するセルが含まれる。 図形には、コントロール ハンドルごとに 1 つの Controls 行が含まれます。 
  
[Controls] 行の名前は Controls. *名前*  を指定し、次のセルを含む。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |ローカル座標での  *図形*  のコントロール ハンドルの位置を示す x 座標を表します。  <br/> |
|[y](y-cell-controls-section.md) <br/> |図形のコントロール ハンドルの位置をローカル座標で示す  *y*  座標を表します。  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |コントロール ハンドルのアンカー ポイントの  *x*  座標をローカル座標で表します。  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |コントロール ハンドル  *のアンカー ポイントの y*  座標をローカル座標で表します。  <br/> |
|[X Behavior](x-behavior-cell-controls-section.md) <br/> |ハンドルの移動後にコントロール ハンドル  *の x*  座標が表示される動作の種類を制御します。  <br/> |
|[Y Behavior](y-behavior-cell-controls-section.md) <br/> |ハンドルの移動後に  *コントロール ハンドルの y*  座標が表示される動作の種類を制御します。  <br/> |
|[Can Glue](can-glue-cell-controls-section.md) <br/> |コントロール ハンドルを他の図形に接着できるかを指定します。  <br/> |
|[ヒント](tip-cell-controls-section.md) <br/> |ツール ヒントとして表示される説明文の文字列を指定します。ツール ヒントは、図形のコントロール ハンドルの上にポインターを重ねたときに表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

 必要に応じて [Controls.  *必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。 既存の [Controls] セクションにコントロール ハンドルを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
これらのセルは行名で参照できます。これは、赤いテキストの ShapeSheet ウィンドウに表示されます。 コントロールにわかりやすい名前を割り当てるには。 *行*  の名前を指定し、行をクリックし、たとえば  *「Custom」*  と入力して、Controls.Custom という行名を作成します。 次に、Controls.Custom.X を使用して [X] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。
  

