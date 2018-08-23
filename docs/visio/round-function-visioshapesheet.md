---
title: ROUND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Numberofdigits によって表される有効桁数に四捨五入します。
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19806260"
---
# <a name="round-function-visioshapesheet"></a>ROUND 関数 (VisioShapeSheet)

*Numberofdigits*によって表される有効桁数に四捨五入します。 
  
## <a name="syntax"></a>構文

ラウンド (* **番号** *、* * *numberofdigits* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**番号** <br/> |四捨五入の対象となる数値を指定します。  <br/> |
| _numberofdigits_ <br/> |必須  <br/> |**番号** <br/> |精度の小数点以下桁数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

_Numberofdigits_が 0 より大きい場合は、小数点の右側に_numberofdigits_で_数値_が丸められます。 _Numberofdigits_が 0 の場合は、_数値_は整数に丸められます。 _Numberofdigits_が 0 より小さい場合は、小数点の左側に_numberofdigits_で_数値_が丸められます。 
  
## <a name="example-1"></a>例 1

ROUND(123.654,2)
  
123.65 を返します。
  
## <a name="example-2"></a>例 2

ROUND(123.654,0)
  
124 を返します。
  
## <a name="example-3"></a>例 3

ROUND(123.654,-1)
  
120 を返します。
  

