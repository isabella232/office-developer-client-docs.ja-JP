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
description: 図形上の1つの接続ポイントに対する x 座標と y 座標、水平方向と垂直方向、および種類を格納します。 接続ポイントの座標は、図形の原点を基準に測定されます。 図形上の各接続ポイントに対して 1 つの [Connection Points] 行があります。
ms.openlocfilehash: 301ea4fb446d9acafd4b59af388c3e7b2d419e20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361027"
---
# <a name="connection-points-row-connection-points-section"></a>[Connection Points] 行 ([Connection Points] セクション)

図形上の1つの接続ポイントに対する*x*座標と*y*座標、水平方向と垂直方向、および種類を格納します。 接続ポイントの座標は、図形の原点を基準に測定されます。 図形上の各接続ポイントに対して 1 つの [Connection Points] 行があります。 
  
[Connection Points] 行に名前が付けられると、それらの名前は [ShapeSheet] ウィンドウで Connections. [シェイプシート] ウィンドウで*名前*を指定します。 [Connection Points] 行には次のセルが含まれます。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |ローカル座標での接続ポイントの*x*座標です。  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |ローカル座標での接続ポイントの*y*座標です。  <br/> |
|[[dirx/A](dirxa-cell-connection-points-section.md) <br/> |一致する接続ポイントの必要な配置ベクトルの*x*コンポーネント。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。  <br/> |
|[[diry/B](diryb-cell-connection-points-section.md) <br/> |一致する接続ポイントの必要な配置ベクトルの*y*コンポーネント。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |接続ポイントの種類 (0 = 内向き; 1 = 外向き; 2 = 内向き + 外向き) です。  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |数式を入力またはテストするために使用できる、スクラッチ セルです。このセルにアクセスするには、行を右クリックしてから、ショートカット メニューの **[図形要素の変更]** をクリックします。<br/> |
   
## <a name="remarks"></a>解説

接続のセル。 [*名前*] 行には、[dirx/A、[diry/B、および Type/C のラベルが付いています。これらの行は拡張または拡張されていない行でもかまいません。 
  
ほとんどの接続ポイント (ユーザー インターフェイスから作成したすべての接続ポイント) は、拡張されていないものであり、DirX、DirY、および Type セルを持っています。行の種類は、**visTagCnnctPt** または **visTagCnnctNamed** になります。
  
拡張された行では、[DirX] および [DirY] セルの両方を使用して、方向のベクトルを定義します。このベクトルは、接続ポイントに基づいて接続されている図形の回転に影響を与えます。定義した値が両方とも 0 の場合は、接続ポイントには方向がありません。接続ポイントには次の種類があります。
  
- 内向き (0)。図形が接続ポイントに接着されることを表します。これは既定値です。
    
- 外向き (1)。接続ポイントが、内向きの接続ポイントに接着されることを表します。
    
- 内向きおよび外向き (2)。方向は内向きですが、外向きの接続として使用する場合は逆になります。
    
拡張された行には [A]、[B]、[C]、および [D] セルがあり、拡張されていない内向きの行が方向を持たなくなったように機能します。通常、拡張された行は使用しません。ただし、データを [A]、[B]、[C]、および [D] セルの接続ポイントに関連付ける場合に使用することがあります。行の種類は、**visTagCnnctPtABCD** または **visTagCnnctNamedABCD** になります。拡張された行は、[D] セルに数式があるかないかで、識別できます。 
  
 必要に応じて [Connections.  必要に応じて行に*名前*を付け、わかりやすい名前を行に割り当て、セルの値を設定します。 既存の [Connection Points] セクションに接続ポイントを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
接続ポイントの行のセルを行名で参照できます。これは、シェイプシートウィンドウで赤いテキストで表示されます。 行名を変更するには、その行名をクリックし、「*カスタム*」などの名前を入力します。たとえば、行名の接続を作成します。 その後、[x] セルを参照することができます。たとえば、またはを使用して、行番号を使用します。 
  
入力する行名は、セクション内で一意の名前にする必要があります。 [Connection Points] セクションで1つの行の名前を作成すると、Microsoft Office Visio によって、セクション内のすべての行の名前が既定の名前である Row_ *n*になります。 
  
名前が付いた [Connection Points] 行は、5.0 より前のバージョンの Visio では使用できません。名前の付いた [Connection Points] 行を持つ Visio の図面ファイルを以前の形式で保存すると、名前の付いた [Connection Points] 行への参照がインデックス付きの参照に変換され、行名は失われます。
  

