---
title: BITOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251400
localization_priority: Normal
ms.assetid: 1d0954c5-b2cb-6c5d-62b3-a68011cf0c85
description: binary number1 または binary number2 の対応するビットが1の場合、各ビットが1に設定された16ビットのバイナリ数値を返します。 binary number1 と binary number2 の両方で対応するビットが0の場合にのみ、ビットが0に設定されます。
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303375"
---
# <a name="bitor-function"></a>BITOR 関数

*binary number1*または*binary number2*の対応するビットが1の場合、各ビットが1に設定された16ビットのバイナリ数値を返します。 *binary number1*と*binary number2*の両方で対応するビットが0の場合にのみ、ビットが0に設定されます。 
  
## <a name="syntax"></a>構文

bitor (* * *binary number1* * *, * * *binary number2* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _二項数値1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _binary number2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

bitor (12, 6)
  
14 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITOR(12,6) = 0...01110 となります。
  

