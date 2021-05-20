---
title: HUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: 色の色相コンポーネントの値を返します。
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439493"
---
# <a name="hue-function"></a>HUE 関数

色の色相コンポーネントの値を返します。
  
## <a name="syntax"></a>構文

HUE(** *expression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |色として評価される式を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

戻り値は 0 ～ 239 の数値です。引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。入力した引数が無効な場合は、0 を返します。 
  
## <a name="example-1"></a>例 1

HUE(Sheet.4!FillForegnd)
  
Sheet.4 について、前景の塗りつぶしの色に関する色合いを返します。
  
## <a name="example-2"></a>例 2

HUE(7)
  
図面で既定の Microsoft Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 7 はシアンを示します。
  
## <a name="example-3"></a>例 3

HUE(HSL(10, 20, 30) )
  
10 を返します。
  

