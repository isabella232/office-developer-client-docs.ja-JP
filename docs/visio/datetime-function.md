---
title: DATETIME 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
ms.localizationpriority: medium
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: datetime または式で表される日付と時刻の値を返します。
ms.openlocfilehash: 2d8d3bd17bf2c89b09b59a203bbe21a33bc6d8f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594637"
---
# <a name="datetime-function"></a>DATETIME 関数

datetime または式で表される日付と時刻  _の値を_ 返  _します_。
  
## <a name="syntax"></a>構文

DATETIME(" ** *datetime* ** "|** *式* ** [, ** *lcid* ** ]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _datetime_ <br/> |必須  <br/> |**String** <br/> |日付および時刻として一般的に認識される任意の文字列、または日付および時刻を含んだセルに対する参照を指定します。  <br/> |
| _expression_ <br/> |必須  <br/> |**String** <br/> |日付および時刻を算出する式を指定します。  <br/> |
| _lcid_ <br/> |オプション  <br/> |**数値** <br/> |現地以外の日時を計算するときに使用するロケール識別子を指定します。ロケール識別子は、システムのヘッダー ファイルに記述されている数字です。  <br/> |
   
### <a name="return-value"></a>戻り値

Datetime
  
## <a name="remarks"></a>注釈

datetime  *が見*  つからないか、有効な日付または時刻として解釈できない場合、DATETIME は日付を返#VALUE! エラーを返します。 
  
戻り値は、システムの現在の [地域] で設定されている短い日付と時刻の形式に従って書式設定されます。 
  
DATETIME 関数は、結果の整数部分が1899 年 12 月 30 日からの日数を表し、小数部が午前 0 時からの 1 日の小数部を表す式の単一の数値値も受け入れられます。 
  
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
  

