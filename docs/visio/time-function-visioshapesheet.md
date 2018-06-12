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
description: 1 時間で表される時刻が返されます、1 分と 1 秒です。
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806667"
---
# <a name="time-function-visioshapesheet"></a>TIME 関数 (VisioShapeSheet)

_時間__分_、および_2 つ目_で表される時刻を返します。
  
## <a name="syntax"></a>構文

時間 (* **時間** *、* **分** *、* * *2* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |必須  <br/> |**数値** <br/> |時間のコンポーネントを指定します。  <br/> |
| _minute_ <br/> |必須  <br/> |**数値** <br/> |分のコンポーネントを指定します。  <br/> |
| _second_ <br/> |必須  <br/> |**数値** <br/> |秒のコンポーネントを指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値
  
## <a name="example-1"></a>例 1

TIME(15,30,30)
  
15:30:30 を表す値を返します。
  
## <a name="example-2"></a>例 2

FORMAT(TIME(15,30,30),"HH:mm")
  
15:30 を表す値を返します。
  
## <a name="example-3"></a>例 3

TIME(15,30,30) + 8 eh.
  
23:30:30 を表す値を返します。
  

