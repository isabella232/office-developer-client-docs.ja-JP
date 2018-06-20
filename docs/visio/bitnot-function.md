---
title: BITNOT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: 2 進数に対応するビットが 0 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
ms.openlocfilehash: 0806e7c52cab659a09d27a60efb9c09aa436fb92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804848"
---
# <a name="bitnot-function"></a>BITNOT 関数

2 進数に対応するビットが 0 である場合にのみでは、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
  
## <a name="syntax"></a>構文

BITNOT (* * *2 進数** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _2 進数_ <br/> |必須  <br/> |**数値** <br/> |16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITNOT(6)
  
65529 を返します。6 = 0...00110 であり、したがって BITNOT(6) = 1...11001 となります。
  

