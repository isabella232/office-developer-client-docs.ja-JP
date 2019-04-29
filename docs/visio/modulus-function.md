---
title: MODULUS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: 数値を除数で割ったときの剰余 (モジュラス) を返します。
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429272"
---
# <a name="modulus-function"></a>MODULUS 関数

数値を除数で割ったときの剰余 (モジュラス) を返します。
  
## <a name="syntax"></a>構文

モジュラス (* **数値** *, * **除数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |被除数 (割られる数) を指定します。  <br/> |
| _序数_ <br/> |必須  <br/> |**数値** <br/> |除数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

結果には除数と同じ符号が付きます。除数が 0 の場合、#DIV/0! エラーを返します。 
  
ほとんどの場合、MOD 関数ではなく MODULUS 関数を使用します。 
  
## <a name="example-1"></a>例 1

MODULUS(5, 1.4)
  
0.8 を返します。
  
## <a name="example-2"></a>例 2

MODULUS(5, -1.4)
  
-0.6 を返します。
  
## <a name="example-3"></a>例 3

MODULUS(-5, 1.4)
  
0.6 を返します。
  
## <a name="example-4"></a>例 4

MODULUS(-5, -1.4)
  
-0.8 を返します。
  

