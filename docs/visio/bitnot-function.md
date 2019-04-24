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
description: バイナリ数の対応するビットが0の場合にのみ、各ビットが1に設定される16ビットのバイナリ数値を返します。 それ以外の場合、ビットは0に設定されます。
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330010"
---
# <a name="bitnot-function"></a>BITNOT 関数

バイナリ数の対応するビットが0の場合にのみ、各ビットが1に設定される16ビットのバイナリ数値を返します。 それ以外の場合、ビットは0に設定されます。
  
## <a name="syntax"></a>構文

bitnot (* **バイナリ番号** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリ番号_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

bitnot (6)
  
65529 を返します。6 = 0...00110 であり、したがって BITNOT(6) = 1...11001 となります。
  

