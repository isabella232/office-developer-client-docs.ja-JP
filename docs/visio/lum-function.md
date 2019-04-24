---
title: LUM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: 色の明度コンポーネントの値を返します。
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357982"
---
# <a name="lum-function"></a>LUM 関数

色の明度コンポーネントの値を返します。
  
## <a name="syntax"></a>構文

LUM (* **式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |図面のカラー テーブルにある色のインデックス、またはカラー インデックスを含むセルに対する参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>解説

戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。 
  
## <a name="example-1"></a>例 1

LUM (シート4[fillforegnd]
  
Sheet.4 について、前景の塗りつぶしの色に関する明度を返します。
  
## <a name="example-2"></a>例 2

LUM (6)
  
図面が既定の Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 6 はマゼンタを示します。
  
## <a name="example-3"></a>例 3

LUM(HSL(10, 20, 30))
  
30 を返します。
  

