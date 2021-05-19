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
description: 時間、分、および秒で表される時間を返します。
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414474"
---
# <a name="time-function-visioshapesheet"></a>TIME 関数 (VisioShapeSheet)

時間、分、および  _秒で表_ される  _時間を_ 返  _します_。
  
## <a name="syntax"></a>構文

TIME(** *hour* **, ** *minute* **, ** *second* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |時間のコンポーネントを指定します。  <br/> |
| _minute_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |分のコンポーネントを指定します。  <br/> |
| _second_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |秒のコンポーネントを指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値型 (Numeric)
  
## <a name="example-1"></a>例 1

TIME(15,30,30)
  
15:30:30 を表す値を返します。
  
## <a name="example-2"></a>例 2

FORMAT(TIME(15,30,30),"HH:mm")
  
15:30 を表す値を返します。
  
## <a name="example-3"></a>例 3

TIME(15,30,30) + 8 eh.
  
23:30:30 を表す値を返します。
  

