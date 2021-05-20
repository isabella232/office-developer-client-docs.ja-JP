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
description: 2 進数値 1 と 2 進数の両方ではなく、対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
ms.openlocfilehash: ab8ff46fe98512d963ef4ecd5c37127353827725
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439234"
---
# <a name="bitxor-function"></a>BITXOR 関数

2 進数値 1 と 2 進数の両方ではなく、対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
  
## <a name="syntax"></a>構文

BITXOR(** *バイナリ番号 1* **, ** *バイナリ番号 2* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリ番号 1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ番号 2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITXOR(12,6)
  
10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。
  

