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
description: x、y で表されるベクトルと x 軸の方向との間の角度を返します。 角度を現在の単位で表した数値を取得できます。
ms.openlocfilehash: 906c024f2a78d6e11c1bbf770c14d04299cadca8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436483"
---
# <a name="atan2-function"></a>ATAN2 関数

*x、y* で表されるベクトルと x 軸の方向との間の角度 *を* 返します。 角度を現在の単位で表した数値を取得できます。 
  
## <a name="syntax"></a>構文

ATAN2(** *y* **, ** *x* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _y_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |ポイント  _の y_-value。  <br/> |
| _x_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |ポイント  _の x_-value。  <br/> |
   
## <a name="remarks"></a>注釈

アークタンジェントは、正の *x* 軸から原点 (0,0) と x と *y* で表される点と交差する線に反時計回りに測定される角度です。 Microsoft Visio では、ATAN2(0,0) は 0 を返します。 ATAN2 の結果を、角度に関する別の測定方法に適用するには、DEG または RAD 関数を使用します。 
  
ATAN2 関数は TAN 関数の逆関数になります。 ATAN2 関数は、角度が  *y*  に等しい角度を x で割った値を返  *します*  。 ATAN2(*y,x*) が直角三角形の角度を表す場合  *、y*  は "反対側  *"、x*  は "隣接側" なので、関数は ATAN2 (反対、隣接) として記述できます。 
  
## <a name="example-1"></a>例 1

ATAN2(1.25,2.25)
  
29.0456°を返します
  
## <a name="example-2"></a>例 2

ATAN2(1,SQRT(3))
  
30°を返します
  
## <a name="example-3"></a>例 3

ATAN2(1,1)
  
45°を返します
  

