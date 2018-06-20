---
title: TIMEVALUE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: 日時または式では、時間値を表すを返しますベースのシステムの地域と言語を設定します。
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806653"
---
# <a name="timevalue-function-visioshapesheet"></a>TIMEVALUE 関数 (VisioShapeSheet)

_日時_または_式_を時間の値を表すを返しますベースのシステムの地域と言語を設定します。
  
## <a name="syntax"></a>構文

TIMEVALUE ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**によって異なります** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
## <a name="remarks"></a>注釈

_日時_または_式_で任意の日付コンポーネントが破棄されます。 
  
_Datetime_が存在しないか、有効な結果に変換することはできません、する場合、この関数は、#VALUE を返す! エラーです。 
  
TIMEVALUE 関数では、結果の小数部分が 1 日午前 0 時からの分数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

TIMEVALUE("6:00 AM")
  
6:00 AM を表す値を返します。
  
## <a name="example-2"></a>例 2

TIMEVALUE("14:30")+4 eh.+30 em.
  
19:00:00 を表す値を返します。
  
## <a name="example-3"></a>例 3

TIMEVALUE("11 AM, July 1, 1997")
  
11:00 AM を表す値を返します。
  
## <a name="example-4"></a>例 4

TIMEVALUE(0.6337)
  
15:12:32 を表す値を返します。
  
## <a name="example-5"></a>例 5

TIMEVALUE("7:89")
  
#VALUE! エラーを返します。
  

