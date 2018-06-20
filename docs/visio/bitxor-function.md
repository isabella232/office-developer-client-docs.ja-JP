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
description: バイナリの数値を 1 とバイナリの数値 2 のどちらかがどちらに対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
ms.openlocfilehash: a0e03258bcfe694dc3bec5469095eff90fb94f1a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804884"
---
# <a name="bitxor-function"></a>BITXOR 関数

バイナリの数値を 1 とバイナリの数値 2 のどちらかがどちらに対応するビットが 1 の場合は、各ビットを 1 に設定するように 16 ビットのバイナリ数値を返します。 それ以外の場合、ビットが 0 に設定されています。
  
## <a name="syntax"></a>構文

BITXOR (* **バイナリ数値 1* * *、* **バイナリ数値 2* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリの数値 1_ <br/> |必須  <br/> |**数値** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ数値 2_ <br/> |必須  <br/> |**数値** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITXOR(12,6)
  
10 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITXOR(12,6) = 0...01010 となります。
  

