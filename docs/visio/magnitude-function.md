---
title: MAGNITUDE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
ms.localizationpriority: medium
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: 立ち上がりが A で、実行が B のベクトルの大きさを、それぞれの定数定数A と定数B を乗算して返します。
ms.openlocfilehash: ac3eb76ad2ad5c20e76f391c6ceedea50d1c3d8d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582506"
---
# <a name="magnitude-function"></a>MAGNITUDE 関数

立ち上がりが  _A_ で、実行が  _B_ のベクトルの大きさを、それぞれの定数  _定数A_ と定数B を掛けた値を  _返します_。 
  
## <a name="syntax"></a>構文

MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |必須かどうか  <br/> |**数値** <br/> |高さを乗算する定数を指定します。  <br/> |
| _A_ <br/> |必須かどうか  <br/> |**数値** <br/> |高さを指定します。  <br/> |
| _constantB_ <br/> |必須かどうか  <br/> |**数値** <br/> |水平距離を乗算する定数を指定します。  <br/> |
| _B_ <br/> |必須かどうか  <br/> |**数値** <br/> |水平距離を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

MAGNITUDE は次の数式に従って計算されます。
  
SQRT((constantA \* A)^2 + (constantB \* B)^2)
  
## <a name="example"></a>例

MAGNITUDE(1, 3, 1, 4) 
  
5 を返します。 
  

