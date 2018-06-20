---
title: '[Connection Points] 行 ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3005
localization_priority: Normal
ms.assetid: eaac62a5-f516-9b81-587a-8e0e02de59ee
description: X と y の座標、水平方向と垂直方向、および図形のポイントの 1 つの接続の種類です。 接続ポイントの座標は、図形の原点から測定されます。 図形には、各コネクション ポイントに対して 1 つの接続ポイント行が含まれています。
ms.openlocfilehash: f1b8daf7f9845b85e76020c7f89c8c42b4500823
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805093"
---
# <a name="connection-points-row-connection-points-section"></a>[Connection Points] 行 ([Connection Points] セクション)

*X*と*y*の座標、水平方向と垂直方向、および図形のポイントの 1 つの接続の種類です。 接続ポイントの座標は、図形の原点から測定されます。 図形には、各コネクション ポイントに対して 1 つの接続ポイント行が含まれています。 
  
接続ポイントの行の名前は、これらの名前は接続として表示されます。 シェイプ シート ウィンドウの*名前*です。 接続ポイントの行には、次のセルが含まれています。 詳細については、特定のセルを参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |*X*の座標をローカル座標での接続ポイントです。  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |*Y*の座標をローカル座標での接続ポイントです。  <br/> |
|[[DirX/A](dirxa-cell-connection-points-section.md) <br/> |*X*に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 動的コネクタに付いている足の向きにも使用します。 このセルでは浮動小数点値です。  <br/> |
|[[DirY/B](diryb-cell-connection-points-section.md) <br/> |*Y*に対応する接続ポイントの必要な整列ベクトルのコンポーネントです。 動的コネクタに付いている足の向きにも使用します。 このセルでは浮動小数点値です。  <br/> |
|[タイプ/C](typec-cell-connection-points-section.md) <br/> |接続ポイントの種類 (0 = 内向き; 1 = 外向き; 2 = 内向き + 外向き) です。  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |数式を入力またはテストするために使用できる、スクラッチ セルです。 このセルにアクセスするには、行を右クリックし、し、ショートカット メニューの [**行の種類の変更**] をクリックします。  <br/> |
   
## <a name="remarks"></a>備考

接続内のセルです。 DirX のラベルが付けられて*名前*」行/A、[DirY/B、および C: と入力/拡張または拡張されていない行は、これらの行があるためです。 
  
ほとんどの接続ポイント (ユーザー インターフェイスによって作成されたすべての接続ポイント) は、拡張されていないと、DirX、DirY、あり、セルの入力です。 その行の種類は、 **visTagCnnctPt**または**visTagCnnctNamed** 。
  
拡張された行では、[DirX] および [DirY] セルの両方を使用して、方向のベクトルを定義します。このベクトルは、接続ポイントに基づいて接続されている図形の回転に影響を与えます。定義した値が両方とも 0 の場合は、接続ポイントには方向がありません。接続ポイントには次の種類があります。
  
- 内向き (0)。図形が接続ポイントに接着されることを表します。これは既定値です。
    
- 外向き (1)。接続ポイントが、内向きの接続ポイントに接着されることを表します。
    
- 内向きおよび外向き (2)。方向は内向きですが、外向きの接続として使用する場合は逆になります。
    
拡張された行は、A、B、C、および D のセルが存在し、内向きの方向性の拡張されていない行のように動作します。 拡張された行は、一般的に使用されていないが、A、B、C、および D のセルでの接続ポイントを持つデータを関連付けるために使用する可能性があります。 その行の種類は、 **visTagCnnctPtABCD**または**visTagCnnctNamedABCD**です。 [D] セルの数式が存在することによって拡張された行を識別できます。 
  
 できるだけ多くの接続を追加できます。  *名前*の行、行に意味のある名前を割り当てるし、セルの値を設定します。 既存の [Connection Points] セクションには、接続ポイントを追加するには、行を右クリックし、ショートカット メニューの [**行の挿入**をクリックします。 
  
接続ポイントの行のセルを参照するには、赤いテキストで、[シェイプ シート] ウィンドウに表示される行名。 行の名前を変更するにはをクリックし、Connections.Custom 行の名前を作成するなどの*ユーザー設定*] などの名前を入力します。 行番号を使用する場合たとえば、Connections.Custom.X または Connections.X1 を使用して [X] セルを参照できます。 
  
入力する行名は、セクション内で一意の名前にする必要があります。 Connection Points] セクションでは、1 つの行の名前を作成するときに Microsoft Office Visio は既定の名前、Connections.Row_ *n* ] セクションで、すべての行の名前です。 
  
名前が付いた [Connection Points] 行は、5.0 より前のバージョンの Visio では使用できません。名前の付いた [Connection Points] 行を持つ Visio の図面ファイルを以前の形式で保存すると、名前の付いた [Connection Points] 行への参照がインデックス付きの参照に変換され、行名は失われます。
  

