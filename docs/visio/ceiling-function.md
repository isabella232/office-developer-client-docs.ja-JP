---
title: CEILING 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
ms.localizationpriority: medium
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: 数値を 0 (ゼロ) から次の複数のインスタンスに切り上げします。 multiple を指定しない場合、数値は 0 から次の整数に丸められます。
ms.openlocfilehash: e544be99fe035e1394d55acb0af5a8ee78e7a06f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578117"
---
# <a name="ceiling-function"></a>CEILING 関数

数値を 0 (ゼロ) から複数の次のインスタンスに切り上  _げします_。 multiple  _を_ 指定しない場合、数値は 0 から次の整数に丸められます。 
  
## <a name="syntax"></a>構文

CEILING(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値** <br/> |切り上げの対象となる数値を指定します。  <br/> |
| _複数_ <br/> |必須かどうか  <br/> |**数値** <br/> |倍数から切り上へ。  <br/> |
   
## <a name="remarks"></a>注釈

 _数値_ と  _倍数は_ 、同じ記号、または複数の記号#NUM! エラーを返します。 数値または  _複数_ の  _値_ に変換できない場合は、値#VALUE! エラーを返します。 数値または _倍数__が_ 0 の場合、結果は 0 になります。 
  
## <a name="example-1"></a>例 1

CEILING(3.7)
  
4 を返します
  
## <a name="example-2"></a>例 2

CEILING(-3.7)
  
-4 を返します
  
## <a name="example-3"></a>例 3

CEILING(3.7, 0.25)
  
3.75 を返します
  

