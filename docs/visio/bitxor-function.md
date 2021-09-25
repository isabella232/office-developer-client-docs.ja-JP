---
title: BITXOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251401
ms.localizationpriority: medium
ms.assetid: 672eacaf-a374-c7e2-b39b-8d42d2371aee
description: 2 進数値 1 と 2 進数の両方ではなく、対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
ms.openlocfilehash: b374eff1fb2644124bb5b4f2a52021d91b00df72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616013"
---
# <a name="bitxor-function"></a>BITXOR 関数

2 進数値 1 と 2 進数の両方ではなく、対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
  
## <a name="syntax"></a>構文

BITXOR(** *バイナリ番号 1* **, ** *バイナリ番号 2* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリ番号 1_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ番号 2_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITXOR(12,6)
  
10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。
  

