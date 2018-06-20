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
description: バイナリ数値 1] または [バイナリの数値を 2 に対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 バイナリの数値を 1 と数値 2 のバイナリの両方に対応するビットは、0 の場合にのみ、ビットは 0 に設定します。
ms.openlocfilehash: db9808f16b32776149abbddf882310c02268cec3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804865"
---
# <a name="bitor-function"></a>BITOR 関数

*バイナリ数値 1* ] または [*バイナリの数値を 2*に対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 ビットは、対応するビットが 0 の*バイナリの数値を 1*と*数値 2 のバイナリ*の両方である場合にのみ、0 に設定されます。 
  
## <a name="syntax"></a>構文

BITOR (* **バイナリ数値 1* * *、* **バイナリ数値 2* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリの数値 1_ <br/> |必須  <br/> |**数値** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ数値 2_ <br/> |必須  <br/> |**数値** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITOR(12,6)
  
14 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITOR(12,6) = 0...01110 となります。
  

