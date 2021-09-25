---
title: BLUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
ms.localizationpriority: medium
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: 色の青いコンポーネントを返します。 戻り値は、0 ~ 255 の範囲の整数です。含まれています。 入力した引数が無効な場合は、0 を返します。
ms.openlocfilehash: eac92b4b83f63d99f65ba7f70cc2dfdcf2634a76
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616006"
---
# <a name="blue-function"></a>BLUE 関数

色の青いコンポーネントを返します。 戻り値は、0 ~ 255 の範囲の整数です。含まれています。 入力した引数が無効な場合は、0 を返します。
  
## <a name="syntax"></a>構文

BLUE(** *expression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="example-1"></a>例 1

BLUE(Sheet.4!FillForegnd)
  
Sheet.4 の前景の塗りつぶしの色に対する青のコンポーネントを返します。
  
## <a name="example-2"></a>例 2

BLUE(13)
  
図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、シアンのインデックスは 13 です。
  
## <a name="example-3"></a>例 3

BLUE(RGB(10, 20, 30))
  
30 を返します。
  

