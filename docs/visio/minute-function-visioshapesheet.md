---
title: MINUTE 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: datetime または expression の分の部分を表す 0 ~ 59 の整数を返します。
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283973"
---
# <a name="minute-function-visioshapesheet"></a>MINUTE 関数 (VisioShapeSheet)

*datetime*または*expression*の分の部分を表す 0 ~ 59 の整数を返します。 
  
## <a name="syntax"></a>構文

分 (" *datetime* " | *式* [, *lcid* ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> | 日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。 ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

整数
  
## <a name="remarks"></a>解説

_datetime_および_expression_の日付コンポーネントは破棄されます。 
  
数値は四捨五入されません。 _datetime_が指定されていない場合、または有効な結果に変換できない場合、関数はエラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている時刻の形式に従って書式設定されます。
  
MINUTE 関数では、 _expression_に単一の数値を使用することもできます。この場合、小数部分には午前0時からの1日の小数を指定します。 
  
## <a name="example-1"></a>例 1

分 ("7/7/1999 13:45:24")
  
45 を返します。
  
## <a name="example-2"></a>例 2

MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)
  
13 を返します。
  
## <a name="example-3"></a>例 3

分 (0.575)
  
48 を返します。
  

