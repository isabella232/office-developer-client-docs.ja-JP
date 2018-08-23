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
description: 色の明度の値を返します。
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805810"
---
# <a name="lum-function"></a>LUM 関数

色の明度の値を返します。
  
## <a name="syntax"></a>構文

明るさ (* **式** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |図面のカラー テーブルにある色のインデックス、またはカラー インデックスを含むセルに対する参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。 
  
## <a name="example-1"></a>例 1

明るさ (Sheet.4!FillForegnd)
  
Sheet.4 について、前景の塗りつぶしの色に関する明度を返します。
  
## <a name="example-2"></a>例 2

LUM(6)
  
図面が既定の Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 6 はマゼンタを示します。
  
## <a name="example-3"></a>例 3

LUM(HSL(10, 20, 30))
  
30 を返します。
  

