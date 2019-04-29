---
title: BLUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: 色の青要素を返します。 戻り値は、0 ~ 255 の範囲の整数です。 入力した引数が無効な場合は、0 を返します。
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439038"
---
# <a name="blue-function"></a>BLUE 関数

色の青要素を返します。 戻り値は、0 ~ 255 の範囲の整数です。 入力した引数が無効な場合は、0 を返します。
  
## <a name="syntax"></a>構文

青 (* **式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**String** <br/> |引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="example-1"></a>例 1

青 (4 枚[fillforegnd]
  
Sheet.4 の前景の塗りつぶしの色に対する青のコンポーネントを返します。
  
## <a name="example-2"></a>例 2

青 (13)
  
図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、シアンのインデックスは 13 です。
  
## <a name="example-3"></a>例 3

BLUE(RGB(10, 20, 30))
  
30 を返します。
  

