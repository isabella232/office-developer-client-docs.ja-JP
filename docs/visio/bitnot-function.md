---
title: BITNOT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
ms.localizationpriority: medium
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: 2 進数の対応するビットが 0 の場合にのみ、各ビットを 1 に設定する 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
ms.openlocfilehash: 66a394ea9627d72e927c0b0cf4a001b4a1994dda
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554874"
---
# <a name="bitnot-function"></a>BITNOT 関数

2 進数の対応するビットが 0 の場合にのみ、各ビットを 1 に設定する 16 ビットのバイナリ番号を返します。 それ以外の場合、ビットは 0 に設定されます。
  
## <a name="syntax"></a>構文

BITNOT(** *バイナリ番号* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリ番号_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITNOT(6)
  
65529 を返します。6 = 0...00110 であり、したがって BITNOT(6) = 1...11001 となります。
  

