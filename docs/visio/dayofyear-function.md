---
title: DAYOFYEAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: 1 ~ 366、日時または式の年の連続した日付を表す整数を返します。 DAYOFYEAR 関数はグレゴリオ暦を使用します。
ms.openlocfilehash: 2fd80a2554c268d276deaa524a9d98eebc6a48d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805208"
---
# <a name="dayofyear-function"></a>DAYOFYEAR 関数

1 ~ 366、_日時_または_式_の年の連続した日付を表す整数を返します。 DAYOFYEAR 関数はグレゴリオ暦を使用します。
  
## <a name="syntax"></a>構文

DAYOFYEAR ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>注釈

_日時_または_式_で任意の時間コンポーネントを破棄します。 
  
結果は、1 月 1 日から 12 月 31 日までに対応します。 丸めは行われません。 _Datetime_が存在しないか、有効な日付または時刻として解釈できない場合、関数はエラーを返します。 
  
DAYOFYEAR 関数は、結果の整数部分が、1899 年 12 月 30 日以降の日数を表す_式_の 1 つの数値値も受け付けます。 
  
## <a name="example-1"></a>例 1

DAYOFYEAR("May 30, 1997 13:45:24")
  
150 を返します。
  
## <a name="example-2"></a>例 2

DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)
  
157 を返します。
  
## <a name="example-3"></a>例 3

DAYOFYEAR(35580.6337)
  
150 を返します。
  

