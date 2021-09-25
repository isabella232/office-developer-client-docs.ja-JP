---
title: TIME 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
ms.localizationpriority: medium
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: 時間、分、および秒で表される時間を返します。
ms.openlocfilehash: 4df859721e4947ba625a473f391d9e81f5606b2e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622747"
---
# <a name="time-function-visioshapesheet"></a>TIME 関数 (VisioShapeSheet)

時間、分、および  _秒で表_ される  _時間を_ 返  _します_。
  
## <a name="syntax"></a>構文

TIME(** *hour* **, ** *minute* **, ** *second* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _hour_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |時間のコンポーネントを指定します。  <br/> |
| _minute_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |分のコンポーネントを指定します。  <br/> |
| _second_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |秒のコンポーネントを指定します。  <br/> |
   
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
  

