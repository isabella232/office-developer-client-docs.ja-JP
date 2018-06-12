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
description: 色の青のコンポーネントを返します。 戻り値は、0 ~ 255 の範囲の整数です。 関数は、無効な入力の場合は 0 を返します。
ms.openlocfilehash: 6a86a0ee91054c89f2def95c0e3521508462bdaa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804907"
---
# <a name="blue-function"></a>BLUE 関数

色の青のコンポーネントを返します。 戻り値は、0 ~ 255 の範囲の整数です。 関数は、無効な入力の場合は 0 を返します。
  
## <a name="syntax"></a>構文

青 (* **式** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

整数
  
## <a name="example-1"></a>例 1

青 (Sheet.4!FillForegnd)
  
Sheet.4 の前景の塗りつぶしの色に対する青のコンポーネントを返します。
  
## <a name="example-2"></a>例 2

BLUE(13)
  
図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、シアンのインデックスは 13 です。
  
## <a name="example-3"></a>例 3

BLUE(RGB(10, 20, 30))
  
30 を返します。
  

