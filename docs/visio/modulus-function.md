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
description: 数値を除数で除算すると余り (剰余) を返します。
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805907"
---
# <a name="modulus-function"></a>MODULUS 関数

数値を除数で除算すると余り (剰余) を返します。
  
## <a name="syntax"></a>構文

剰余 (* **番号** *、* **除数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**番号** <br/> |被除数 (割られる数) を指定します。  <br/> |
| _除数_ <br/> |必須  <br/> |**番号** <br/> |除数を指定します。  <br/> |
   
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
  

