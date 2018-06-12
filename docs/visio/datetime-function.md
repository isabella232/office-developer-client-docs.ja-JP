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
description: 日時または式で表される日付と時刻の値を返します。
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805185"
---
# <a name="datetime-function"></a>DATETIME 関数

_日時_または_式_で表される日付と時刻の値を返します。
  
## <a name="syntax"></a>構文

DATETIME ("* * *datetime* * *」。* **式** * [、* * *lcid* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _日付時刻_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |省略可能  <br/> |**番号** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>�߂�l

日付/時刻
  
## <a name="remarks"></a>注釈

*Datetime*が存在しないか、有効な日付または時刻として解釈できない場合、日付時刻は、#VALUE を返します。 エラーです。 
  
戻り値は、システムの現在の [地域] で設定されている短い日付と時刻の形式に従って書式設定されます。 
  
DATETIME 関数では、*式*結果の整数部分は 1899 年 12 月 30 日以降の日数を表し、午前 0 時から 1 日の端数を表す小数部分の数値が 1 つも受け付けます。 
  
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

DATETIME(35580.6337)
  
1997/5/30 午後 3:12:32 を表す値を返します。
  

