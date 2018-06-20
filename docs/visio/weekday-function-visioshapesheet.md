---
title: WEEKDAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: 日時または式の曜日を表す 1 ~ 7 の整数を返します。
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806789"
---
# <a name="weekday-function-visioshapesheet"></a>WEEKDAY 関数 (VisioShapeSheet)

_日時_または_式_の曜日を表す 1 ~ 7 の整数を返します。
  
## <a name="syntax"></a>構文

平日 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**によって異なります** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>�߂�l

整数型 (Integer)
  
## <a name="remarks"></a>Remarks

_日時_または_式_の時間の構成要素は破棄されます。 
  
結果は、(1) を月曜日から日曜日 (7) に対応します。 丸めは行われません。 _Datetime_が存在しないか、有効な日付または時刻として解釈できない場合、関数は #value! を返します。 エラーです。 
  
WEEKDAY 関数では、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

WEEKDAY("May 30, 1999")
  
7 を返します。
  
## <a name="example-2"></a>例 2

WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)
  
2 を返します。
  
## <a name="example-3"></a>例 3

WEEKDAY(35880.6337)
  
4 を返します。
  

