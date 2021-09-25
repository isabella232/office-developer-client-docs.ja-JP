---
title: MODULUS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
ms.localizationpriority: medium
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: 数値を除算で割った場合の残余 (モジュラス) を返します。
ms.openlocfilehash: 6d6d9893800aa8db0e882dd92d4adb0d05acb930
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623335"
---
# <a name="modulus-function"></a>MODULUS 関数

数値を除算で割った場合の残余 (モジュラス) を返します。
  
## <a name="syntax"></a>構文

MODULUS(** *number* **, ** *divisor* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値** <br/> |被除数 (割られる数) を指定します。  <br/> |
| _divisor_ <br/> |必須かどうか  <br/> |**数値** <br/> |除数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
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
  

