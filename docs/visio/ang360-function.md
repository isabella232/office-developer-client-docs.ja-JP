---
title: ANG360 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
ms.localizationpriority: medium
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: 角度の範囲を正規化します。
ms.openlocfilehash: b94af0ea3d20c839f9bb314e042b2c19da0f0820
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603943"
---
# <a name="ang360-function"></a>ANG360 関数

角度の範囲を 0 = 結果 \< \< 2PI ラジアン (0 = 結果 \< \< 360 度) に正規化します。
  
## <a name="syntax"></a>構文

ANG360(***angle*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _angle_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |正規化する角度を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

角度  *単位*  を使用して角度を指定しない場合は、ラジアンとして解釈されます。 angle  *を*  値に変換できない場合は、値#VALUE! を返します。 
  
## <a name="example-1"></a>例 1

ANG360(395 deg)
  
35°を返します
  
## <a name="example-2"></a>例 2

ANG360(-9.8 rad)
  
2.7664 ラジアンを返します
  
## <a name="example-3"></a>例 3

ANG360(45)
  
58.31° (1.0177 ラジアン) を返します
  

