---
title: ATAN2 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251397
localization_priority: Normal
ms.assetid: 524278fb-196e-9cf9-e27b-d03642beeee4
description: X によって表されるベクトルの角度を返します。 y、x 方向の軸。 角度の測定の現在の単位の数値になります。
ms.openlocfilehash: dfd62ce628a3a46ff14b3ffc3f07074a39c66e14
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804772"
---
# <a name="atan2-function"></a>ATAN2 関数

*X、y*および*x*の方向によって表されるベクトルの角度を返します-軸です。 角度の測定の現在の単位の数値になります。 
  
## <a name="syntax"></a>構文

ATAN2 (* * *y* * *、* * *x* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |_Y_-点の値です。  <br/> |
| _x_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |_X_-点の値です。  <br/> |
   
## <a name="remarks"></a>注釈

アーク タンジェントは、正の*x*から反時計回りに測定する角度の原点 (0, 0) および*x*と*y*で表される点を通る直線を軸。 Microsoft Visio では、ATAN2(0,0) は 0 を返します。 ATAN2 の結果を別の角度の測定を強制するには、DEG または RAD 関数を使用します。 
  
ATAN2 関数は、TAN 関数の antifunction です。 ATAN2 関数が返す角度は、 *y*を*x*で割った値に等しい角度です。 場合 ATAN2 (*y, x*) は、直角三角形の角度を表す、 *y*は「反対側の辺」、および atan2 関数が書き込まれるために、 *x*は「隣接する辺」。 
  
## <a name="example-1"></a>例 1

ATAN2(1.25,2.25)
  
29.0456°を返します
  
## <a name="example-2"></a>例 2

ATAN2(1,SQRT(3))
  
30°を返します
  
## <a name="example-3"></a>例 3

ATAN2(1,1)
  
45°を返します
  

