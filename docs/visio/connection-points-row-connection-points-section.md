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
description: x 座標と y 座標、水平方向と垂直方向を含み、図形上の 1 つの接続ポイントを入力します。 接続ポイントの座標は、図形の原点を基準に測定されます。 図形上の各接続ポイントに対して 1 つの [Connection Points] 行があります。
ms.openlocfilehash: 301ea4fb446d9acafd4b59af388c3e7b2d419e20
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415510"
---
# <a name="connection-points-row-connection-points-section"></a>[Connection Points] 行 ([Connection Points] セクション)

x 座標と *y* 座標、水平方向と垂直方向を含み、図形上の 1 つの接続ポイントを入力します。  接続ポイントの座標は、図形の原点を基準に測定されます。 図形上の各接続ポイントに対して 1 つの [Connection Points] 行があります。 
  
[Connection Points] 行に名前が付けられると、それらの名前は [ShapeSheet] ウィンドウで Connections. *[シェイプ*  シート] ウィンドウの名前を指定します。 [Connection Points] 行には次のセルが含まれます。 詳細については、各セルに関連する項目を参照してください。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-connection-points-section.md) <br/> |ローカル  *座標*  の接続ポイントの x 座標。  <br/> |
|[Y](y-cell-connection-points-section.md) <br/> |ローカル  *座標の*  接続ポイントの y 座標。  <br/> |
|[DirX/A](dirxa-cell-connection-points-section.md) <br/> |一  *致する*  接続ポイントの必要な配置ベクトルの x -component。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。  <br/> |
|[DirY/B](diryb-cell-connection-points-section.md) <br/> |一  *致する接続*  ポイントの必要な配置ベクトルの y -component。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。  <br/> |
|[Type/C](typec-cell-connection-points-section.md) <br/> |接続ポイントの種類 (0 = 内向き; 1 = 外向き; 2 = 内向き + 外向き) です。  <br/> |
|[D](d-cell-connection-points-section.md) <br/> |数式を入力またはテストするために使用できる、スクラッチ セルです。このセルにアクセスするには、行を右クリックしてから、ショートカット メニューの **[図形要素の変更]** をクリックします。<br/> |
   
## <a name="remarks"></a>注釈

Connections 内のセル。 *これらの*  行は拡張または拡張されていない行が可能なので、name 行には DirX/A、DirY/B、Type/C というラベルが付けされます。 
  
ほとんどの接続ポイント (ユーザー インターフェイスから作成したすべての接続ポイント) は、拡張されていないものであり、DirX、DirY、および Type セルを持っています。行の種類は、**visTagCnnctPt** または **visTagCnnctNamed** になります。
  
拡張された行では、[DirX] および [DirY] セルの両方を使用して、方向のベクトルを定義します。このベクトルは、接続ポイントに基づいて接続されている図形の回転に影響を与えます。定義した値が両方とも 0 の場合は、接続ポイントには方向がありません。接続ポイントには次の種類があります。
  
- 内向き (0)。図形が接続ポイントに接着されることを表します。これは既定値です。
    
- 外向き (1)。接続ポイントが、内向きの接続ポイントに接着されることを表します。
    
- 内向きおよび外向き (2)。方向は内向きですが、外向きの接続として使用する場合は逆になります。
    
拡張された行には [A]、[B]、[C]、および [D] セルがあり、拡張されていない内向きの行が方向を持たなくなったように機能します。通常、拡張された行は使用しません。ただし、データを [A]、[B]、[C]、および [D] セルの接続ポイントに関連付ける場合に使用することがあります。行の種類は、**visTagCnnctPtABCD** または **visTagCnnctNamedABCD** になります。拡張された行は、[D] セルに数式があるかないかで、識別できます。 
  
 必要に応じて [Connections.  *必要に*  応じて行に名前を付け、行にわかりやすい名前を割り当て、セル値を設定します。 既存の [Connection Points] セクションに接続ポイントを追加するには、行を右クリックして、ショートカット メニューの **[行の挿入]** をクリックします。 
  
[接続ポイント] 行のセルは、赤いテキストの [シェイプシート] ウィンドウに表示される行名で参照できます。 行名を変更するには、行名をクリックし、たとえば、行名Connections.Custom を作成する場合は、カスタムなどの名前を入力します。 行番号を使用する場合は、Connections.Custom.X を使用して[X] セルを参照できます。たとえば、Connections.X1 を使用します。 
  
入力する行名は、セクション内で一意の名前にする必要があります。 [接続ポイント] セクションで 1 行の名前を作成するとMicrosoft Office Visioセクション内のすべての行に既定の名前 n を付Connections.Row_ *します*。 
  
名前が付いた [Connection Points] 行は、5.0 より前のバージョンの Visio では使用できません。名前の付いた [Connection Points] 行を持つ Visio の図面ファイルを以前の形式で保存すると、名前の付いた [Connection Points] 行への参照がインデックス付きの参照に変換され、行名は失われます。
  

