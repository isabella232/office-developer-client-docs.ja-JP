---
title: 日付、時刻、期間の値について
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm82251852
localization_priority: Normal
ms.assetid: b6951a92-f32a-5829-5e07-b277b7934df3
description: 日付、時刻、期間の値を使用して数式の操作を行うことができます。 Microsoft Visio では、日付と時刻の式を 1 つの値として評価できます。 日付と時刻の式とは、日付や時刻、または日付や時刻を含むセルへの参照として一般的に認識されるすべての式を指します。 この式には、日付および時刻として判断される文字列や数値、および関数から返される日付と時刻の値も含まれます。
ms.openlocfilehash: 936055ed6d13b75bd0c42c95564046a76082ec0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804744"
---
# <a name="about-date-time-and-duration-values"></a>日付、時刻、期間の値について

日付、時刻、期間の値を使用して数式の操作を行うことができます。 Microsoft Visio では、日付と時刻の式を 1 つの値として評価できます。 日付と時刻の式とは、日付や時刻、または日付や時刻を含むセルへの参照として一般的に認識されるすべての式を指します。 この式には、日付および時刻として判断される文字列や数値、および関数から返される日付と時刻の値も含まれます。
  
Visio では、日付と時刻の値は 64 桁の浮動小数値として内部的に保存されます。 小数点の左側にある値は、1899 年 12 月 30 日からの通算日を示しています。 小数点の右側にある値は、午前 0 時からの経過時間を 1 日に対する割合で示しています。 正午は .5 と表されます。
  
単一の定数としてではなく、式で日付と時刻を使用するには、日付と時刻の値であることを識別するために適切な関数を使用する必要があります。
  
## <a name="valid-dates"></a>有効な日付

||||
|:-----|:-----|:-----|
| "2/28"  <br/> | "2/28/99"  <br/> | "2/28/1999"  <br/> |
| "2-28"  <br/> | "2-28-99"  <br/> | "2-28/1999"  <br/> |
| "6 Mar 99"  <br/> | "6 Mar"  <br/> | "6 Mar 99"  <br/> |
| "1 January 99"  <br/> | "Jan 1, 99"  <br/> | "Jan 1, 1999"  <br/> |
| "Jan 00"  <br/> | "January, 2000"  <br/> | "Jan 1, 00"  <br/> |
   
## <a name="valid-times"></a>有効な時刻

||||
|:-----|:-----|:-----|
| "3:45"  <br/> | "3:45:27"  <br/> | "7a"  <br/> |
| "7 am"  <br/> | "7 p"  <br/> | "7:30 PM"  <br/> |
   
## <a name="date-and-time-functions"></a>日付と時刻の関数

|**Function**|**説明**|
|:-----|:-----|
|[DATE](date-function-visioshapesheet.md) <br/> | 数値を日付の値に変換します。  <br/> |
|[DATETIME](datetime-function.md) <br/> | 文字列を日付と時刻の値に変換します。  <br/> |
|[DATEVALUE](datevalue-function-visioshapesheet.md) <br/> | 文字列を日付の値に変換します。  <br/> |
|[NOW](now-function-visioshapesheet.md) <br/> | 現在のシステムの日付を日付と時刻の値として返します。  <br/> |
|[TIME](time-function-visioshapesheet.md) <br/> | 数値を時刻の値に変換します。  <br/> |
|[TIMEVALUE](timevalue-function-visioshapesheet.md) <br/> | 文字列を時刻の値に変換します。  <br/> |
|[DAY](day-function-visioshapesheet.md) <br/> | 日付のうち、日を日付と時刻の式として返します。  <br/> |
|[DAYOFYEAR](dayofyear-function.md) <br/> | 年の何日目かを表す値を日付と時刻の式として返します。  <br/> |
|[HOUR](hour-function-visioshapesheet.md) <br/> | 時刻のうち、時間を日付と時刻の式として返します。  <br/> |
|[MINUTE](minute-function-visioshapesheet.md) <br/> | 時刻のうち、分を日付と時刻の式として返します。  <br/> |
|[MONTH](month-function-visioshapesheet.md) <br/> | 日付のうち、月を日付と時刻の式として返します。  <br/> |
|[SECOND](second-function-visioshapesheet.md) <br/> | 時刻のうち、秒を日付と時刻の式として返します。  <br/> |
|[WEEKDAY](weekday-function-visioshapesheet.md) <br/> | 曜日の番号を日付と時刻の式として返します。  <br/> |
|[YEAR](year-function-visioshapesheet.md) <br/> | 日付のうち、年を日付と時刻の式として返します。  <br/> |
   
## <a name="duration"></a>期間

期間または経過時間を計算する演算を実行できます。期間は、内部的には日数と時間を表す小数部分から成る形式で保存されます。たとえば、1 週間経過、7 日間経過、および 168 時間経過は、すべて内部的には 7.0 として保存されますが、表示には適切な単位で表示されます。
  
Visio は、次の表にある期間の単位を認識します。
  
|**単位**|**略語**|**汎用省略形**|
|:-----|:-----|:-----|
| 経過した日数  <br/> | eday, ed.  <br/> | ed  <br/> |
| 経過した時間  <br/> | ehour, eh.  <br/> | eh  <br/> |
| 経過した分数  <br/> | eminute, em.  <br/> | em  <br/> |
| 経過した秒数  <br/> | esecond, es.  <br/> | es  <br/> |
| 経過した週数  <br/> | eweek, ew.  <br/> | ew  <br/> |
   
期間に日付と時刻を加えて、新しい日付と時刻を計算できます。日付、時刻、期間を使用して、次の表に示される演算を実行できます。
  
|**入力**|**結果**|
|:-----|:-----|
| 日付-時刻 +/- 期間  <br/> | 日付と時刻の値  <br/> |
| 期間 +/- 日付-時刻  <br/> | 日付と時刻の値  <br/> |
| 期間 +/- 期間  <br/> | 期間の値  <br/> |
| 日付-時間 + 日付-時間  <br/> | 日付と時刻の値  <br/> |
| 日付-時間 - 日付-時間  <br/> | 期間の値  <br/> |
   

