---
title: BITXOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
localization_priority: Normal
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: 各ビットが1に設定された16ビットのバイナリ数値を返します。 binary number1 と binary number2 の両方ではなく対応するビットが1に設定されています。 それ以外の場合、ビットは0に設定されます。
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302990"
---
# <a name="bitxor-function"></a>BITXOR 関数

各ビットが1に設定された16ビットのバイナリ数値を返します。 binary number1 と binary number2 の両方ではなく対応するビットが1に設定されています。 それ以外の場合、ビットは0に設定されます。
  
## <a name="syntax"></a>構文

bitxor (* * *binary number1* * *, * * *binary number2* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _二項数値1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _binary number2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

bitxor (12, 6)
  
10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。
  

