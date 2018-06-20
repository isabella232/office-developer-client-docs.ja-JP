---
title: DAY 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: 日時または式の曜日を表す 1 ~ 31 の整数を返します。 DAY 関数はグレゴリオ暦を使用します。
ms.openlocfilehash: 07607b809aec9f50ae8981476313fc5e8dbc3423
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805198"
---
# <a name="day-function-visioshapesheet"></a>DAY 関数 (VisioShapeSheet)

_日時_または_式_の日を表す 1 ~ 31 の整数を返します。 DAY 関数はグレゴリオ暦を使用します。
  
## <a name="syntax"></a>構文

日 ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>�߂�l

整数型 (Integer)
  
## <a name="remarks"></a>Remarks

_日時_または_式_で任意の時間コンポーネントを破棄します。 
  
丸めは行われません。 _Datetime_が存在しないか、有効な結果に変換することはできません、する場合、関数はエラーを返します。 
  
DAY 関数では、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

DAY("May 30, 1997 15:45:24")
  
30 を返します。
  
## <a name="example-2"></a>例 2

DAY(DATEVALUE("May 30, 1997")+7 ed.)
  
6 を返します。
  
## <a name="example-3"></a>例 3

DAY(35580.6337)
  
30 を返します。
  

