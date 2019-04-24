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
description: datetime または expression の年の何日目かを表す、1 ~ 366 の整数を返します。 DAYOFYEAR 関数では、グレゴリオ暦が使用されます。
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360294"
---
# <a name="dayofyear-function"></a>DAYOFYEAR 関数

_datetime_または_expression_の年の何日目かを表す、1 ~ 366 の整数を返します。 DAYOFYEAR 関数では、グレゴリオ暦が使用されます。
  
## <a name="syntax"></a>構文

DAYOFYEAR ("* * *datetime* * *" |* **式** * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>解説

_datetime_または_expression_の時刻コンポーネントは破棄されます。 
  
結果は 1 月 1 日～ 12 月 31 日に対応します。 数値は四捨五入されません。 _datetime_が指定されていない場合、または有効な日付または時刻として解釈できない場合は、関数はエラーを返します。 
  
DAYOFYEAR 関数では、 _expression_に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定します。 
  
## <a name="example-1"></a>例 1

DAYOFYEAR("May 30, 1997 13:45:24")
  
150 を返します。
  
## <a name="example-2"></a>例 2

DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)
  
157 を返します。
  
## <a name="example-3"></a>例 3

DAYOFYEAR (35580.6337)
  
150 を返します。
  

