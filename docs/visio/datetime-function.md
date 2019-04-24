---
title: DATETIME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: datetime または expression で表される日付と時刻の値を返します。
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360320"
---
# <a name="datetime-function"></a>DATETIME 関数

_datetime_または_expression_で表される日付と時刻の値を返します。
  
## <a name="syntax"></a>構文

datetime ("* * *datetime* * *" |* **式** * [, * * *lcid* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

Datetime
  
## <a name="remarks"></a>解説

*datetime*が指定されていない場合、または有効な日付または時刻として解釈できない場合は、datetime は #VALUE を返します。 エラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている短い日付と時刻の形式に従って書式設定されます。 
  
DATETIME 関数では、 *expression*に単一の数値を使用することもできます。この場合、整数部分には1899年12月30日から起算した日数を指定し、小数部分には午前0時からの日数を指定します。 
  
## <a name="example-1"></a>例 1

DATETIME("May 30, 1997")+5 ed.
  
1997/6/4 を表す値を返します。
  
## <a name="example-2"></a>例 2

FORMAT(DATETIME("5/20/1997 14:30:45"),"C")
  
文字列 "Tuesday, May 20, 1997 2:30:45 PM" を返します。
  
## <a name="example-3"></a>例 3

DATETIME("1:30 PM July 19")
  
2001/7/19 午後 1:30:00 を表す値 (現在の年を 2001 とする) を返します。
  
## <a name="example-4"></a>例 4

DATETIME (35580.6337)
  
1997/5/30 午後 3:12:32 を表す値を返します。
  

