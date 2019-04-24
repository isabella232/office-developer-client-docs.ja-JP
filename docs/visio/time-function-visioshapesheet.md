---
title: TIME 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: hour、minute、および second で表される時間を返します。
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280998"
---
# <a name="time-function-visioshapesheet"></a>TIME 関数 (VisioShapeSheet)

_hour_、 _minute_、および_second_で表される時間を返します。
  
## <a name="syntax"></a>構文

時刻 (* **時** *、* **分** *、* **秒** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |時間のコンポーネントを指定します。  <br/> |
| _minute_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |分のコンポーネントを指定します。  <br/> |
| _second_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |秒のコンポーネントを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値型 (Numeric)
  
## <a name="example-1"></a>例 1

時間 (15、30、30)
  
15:30:30 を表す値を返します。
  
## <a name="example-2"></a>例 2

FORMAT (TIME (15, 30, 30), "HH: mm")
  
15:30 を表す値を返します。
  
## <a name="example-3"></a>例 3

TIME(15,30,30) + 8 eh.
  
23:30:30 を表す値を返します。
  

