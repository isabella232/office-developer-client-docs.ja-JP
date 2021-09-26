---
title: SAT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
ms.localizationpriority: medium
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: 色の彩度コンポーネントの値を返します。
ms.openlocfilehash: 619a221e1b22442605364ee8cdf1b29f3fc002c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627549"
---
# <a name="sat-function"></a>SAT 関数

色の彩度コンポーネントの値を返します。 
  
## <a name="syntax"></a>構文

SAT(** *式* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須かどうか  <br/> |**さまざま** <br/> |引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値型 (Numeric)
  
## <a name="remarks"></a>注釈

戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。
  
## <a name="example-1"></a>例 1

SAT(Sheet.4!FillForegnd)
  
Sheet.4 について、前景の塗りつぶしの色に関する彩度を返します。
  
## <a name="example-2"></a>例 2

SAT(8)
  
図面が既定の Visio カラー パレットを使用する場合、240 を返します。Visio カラー パレットでは、インデックス 8 は濃い赤を示します。
  
## <a name="example-3"></a>例 3

SAT(HSL(10, 20, 30))
  
20 を返します。
  

