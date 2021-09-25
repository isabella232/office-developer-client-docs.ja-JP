---
title: LUM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
ms.localizationpriority: medium
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: 色の光度コンポーネントの値を返します。
ms.openlocfilehash: 752af49222ed7919e6c7b9cce4a51821bbe9f4b7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582526"
---
# <a name="lum-function"></a>LUM 関数

色の光度コンポーネントの値を返します。
  
## <a name="syntax"></a>構文

LUM(** *expression* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _expression_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |図面のカラー テーブルにある色のインデックス、またはカラー インデックスを含むセルに対する参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。 
  
## <a name="example-1"></a>例 1

LUM(Sheet.4!FillForegnd)
  
Sheet.4 について、前景の塗りつぶしの色に関する明度を返します。
  
## <a name="example-2"></a>例 2

LUM(6)
  
図面が既定の Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 6 はマゼンタを示します。
  
## <a name="example-3"></a>例 3

LUM(HSL(10, 20, 30))
  
30 を返します。
  

