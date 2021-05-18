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
description: 2 進数 1 または 2 進数の対応するビットが 1 の場合、各ビットが 1 に設定されている 16 ビットのバイナリ番号を返します。 ビットが 0 に設定されているのは、対応するビットがバイナリ番号 1 とバイナリ番号 2 の両方で 0 の場合のみです。
ms.openlocfilehash: 13bda2c6c65557b1f8372432cf919b2aaf2d75de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408083"
---
# <a name="bitor-function"></a>BITOR 関数

2 進数 1 または *2* 進数の対応するビットが 1 の場合、各ビットが *1* に設定されている 16 ビットのバイナリ番号を返します。 ビットが 0 に設定されているのは、対応するビットがバイナリ番号  *1*  とバイナリ番号 2 の両方で 0  *の場合のみです*  。 
  
## <a name="syntax"></a>構文

BITOR(** *バイナリ番号 1* **, ** *バイナリ番号 2* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _バイナリ番号 1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の 16 ビットのバイナリ数値を指定します。  <br/> |
| _バイナリ番号 2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の 16 ビットのバイナリ数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

16 ビットのバイナリ数値
  
## <a name="example"></a>例

BITOR(12,6)
  
14 を返します。12 = 0...01100、6 = 0...00110 であり、したがって BITOR(12,6) = 0...01110 となります。
  

