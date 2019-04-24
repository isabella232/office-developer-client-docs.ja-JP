---
title: ANG360 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: 角度の範囲を正規化します。
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341490"
---
# <a name="ang360-function"></a>ANG360 関数

角度の\<範囲を 0 = result \< 2pi ラジアンに正規化します\<(0 \< = result 360 度)。
  
## <a name="syntax"></a>構文

ANG360 (* * *angle* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _直交_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |正規化する角度を指定します。  <br/> |
   
## <a name="remarks"></a>解説

角度を指定しない場合、*角度*はラジアンとして解釈されます。 *角度*を値に変換できない場合は、#VALUE します。 を返します。 
  
## <a name="example-1"></a>例 1

ANG360(395 deg)
  
35°を返します
  
## <a name="example-2"></a>例 2

ANG360(-9.8 rad)
  
2.7664 ラジアンを返します
  
## <a name="example-3"></a>例 3

ANG360 (45)
  
58.31° (1.0177 ラジアン) を返します
  

