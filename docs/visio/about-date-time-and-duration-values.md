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
ms.openlocfilehash: 56de919fa713c0948bb87f794d1c6e0a5d727aef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341581"
---
# <a name="about-date-time-and-duration-values"></a><span data-ttu-id="2ab90-106">日付、時刻、期間の値について</span><span class="sxs-lookup"><span data-stu-id="2ab90-106">About Date, Time, and Duration Values</span></span>

<span data-ttu-id="2ab90-107">日付、時刻、期間の値を使用して数式の操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-107">You can perform operations in formulas using date, time, and duration values.</span></span> <span data-ttu-id="2ab90-108">Microsoft Visio では、日付と時刻の式を 1 つの値として評価できます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-108">In Microsoft Visio, a date and time expression can be evaluated as a single value.</span></span> <span data-ttu-id="2ab90-109">日付と時刻の式とは、日付や時刻、または日付や時刻を含むセルへの参照として一般的に認識されるすべての式を指します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-109">A date and time expression is any expression commonly recognized as a date and/or time or a reference to a cell containing a date and/or time.</span></span> <span data-ttu-id="2ab90-110">この式には、日付および時刻として判断される文字列や数値、および関数から返される日付と時刻の値も含まれます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-110">This includes strings and numbers that look like a date and time, and date and time values returned from functions.</span></span>
  
<span data-ttu-id="2ab90-111">Visio では、日付と時刻の値は 64 桁の浮動小数値として内部に保存されます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-111">Date and time values in Visio are stored internally as a 64-bit floating point number.</span></span> <span data-ttu-id="2ab90-112">小数点の左側にある値は、1899 年 12 月 30 日からの通算日を示しています。</span><span class="sxs-lookup"><span data-stu-id="2ab90-112">The value to the left of the decimal represents the number of days since December 30, 1899.</span></span> <span data-ttu-id="2ab90-113">小数点の右側にある値は、午前 0 時からの経過時間を 1 日に対する割合で示しています。</span><span class="sxs-lookup"><span data-stu-id="2ab90-113">The value to the right of the decimal represents the fraction of a day since midnight.</span></span> <span data-ttu-id="2ab90-114">正午は .5 と表されます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-114">Noon is represented by .5.</span></span>
  
<span data-ttu-id="2ab90-115">単一の定数としてではなく、式で日付と時刻を使用するには、日付と時刻の値であることを識別するために適切な関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2ab90-115">To use dates and times within an expression (rather than as a single constant), you must use the appropriate function to identify them as date and time values.</span></span>
  
## <a name="valid-dates"></a><span data-ttu-id="2ab90-116">有効な日付</span><span class="sxs-lookup"><span data-stu-id="2ab90-116">Valid dates</span></span>

||||
|:-----|:-----|:-----|
| <span data-ttu-id="2ab90-117">"2/28"</span><span class="sxs-lookup"><span data-stu-id="2ab90-117">"2/28"</span></span>  <br/> | <span data-ttu-id="2ab90-118">"2/28/99"</span><span class="sxs-lookup"><span data-stu-id="2ab90-118">"2/28/99"</span></span>  <br/> | <span data-ttu-id="2ab90-119">"2/28/1999"</span><span class="sxs-lookup"><span data-stu-id="2ab90-119">"2/28/1999"</span></span>  <br/> |
| <span data-ttu-id="2ab90-120">"2-28"</span><span class="sxs-lookup"><span data-stu-id="2ab90-120">"2-28"</span></span>  <br/> | <span data-ttu-id="2ab90-121">"2-28-99"</span><span class="sxs-lookup"><span data-stu-id="2ab90-121">"2-28-99"</span></span>  <br/> | <span data-ttu-id="2ab90-122">"2-28/1999"</span><span class="sxs-lookup"><span data-stu-id="2ab90-122">"2-28/1999"</span></span>  <br/> |
| <span data-ttu-id="2ab90-123">"6 Mar 99"</span><span class="sxs-lookup"><span data-stu-id="2ab90-123">"6 Mar 99"</span></span>  <br/> | <span data-ttu-id="2ab90-124">"6 Mar"</span><span class="sxs-lookup"><span data-stu-id="2ab90-124">"6 Mar"</span></span>  <br/> | <span data-ttu-id="2ab90-125">"6 Mar 99"</span><span class="sxs-lookup"><span data-stu-id="2ab90-125">"6 Mar 99"</span></span>  <br/> |
| <span data-ttu-id="2ab90-126">"1 January 99"</span><span class="sxs-lookup"><span data-stu-id="2ab90-126">"1 January 99"</span></span>  <br/> | <span data-ttu-id="2ab90-127">"Jan 1, 99"</span><span class="sxs-lookup"><span data-stu-id="2ab90-127">"Jan 1, 99"</span></span>  <br/> | <span data-ttu-id="2ab90-128">"Jan 1, 1999"</span><span class="sxs-lookup"><span data-stu-id="2ab90-128">"Jan 1, 1999"</span></span>  <br/> |
| <span data-ttu-id="2ab90-129">"Jan 00"</span><span class="sxs-lookup"><span data-stu-id="2ab90-129">"Jan 00"</span></span>  <br/> | <span data-ttu-id="2ab90-130">"January, 2000"</span><span class="sxs-lookup"><span data-stu-id="2ab90-130">"January, 2000"</span></span>  <br/> | <span data-ttu-id="2ab90-131">"Jan 1, 00"</span><span class="sxs-lookup"><span data-stu-id="2ab90-131">"Jan 1, 00"</span></span>  <br/> |
   
## <a name="valid-times"></a><span data-ttu-id="2ab90-132">有効な時刻</span><span class="sxs-lookup"><span data-stu-id="2ab90-132">Valid times</span></span>

||||
|:-----|:-----|:-----|
| <span data-ttu-id="2ab90-133">"3:45"</span><span class="sxs-lookup"><span data-stu-id="2ab90-133">"3:45"</span></span>  <br/> | <span data-ttu-id="2ab90-134">"3:45:27"</span><span class="sxs-lookup"><span data-stu-id="2ab90-134">"3:45:27"</span></span>  <br/> | <span data-ttu-id="2ab90-135">"7a"</span><span class="sxs-lookup"><span data-stu-id="2ab90-135">"7a"</span></span>  <br/> |
| <span data-ttu-id="2ab90-136">"7 am"</span><span class="sxs-lookup"><span data-stu-id="2ab90-136">"7 am"</span></span>  <br/> | <span data-ttu-id="2ab90-137">"7 p"</span><span class="sxs-lookup"><span data-stu-id="2ab90-137">"7 p"</span></span>  <br/> | <span data-ttu-id="2ab90-138">"7:30 PM"</span><span class="sxs-lookup"><span data-stu-id="2ab90-138">"7:30 PM"</span></span>  <br/> |
   
## <a name="date-and-time-functions"></a><span data-ttu-id="2ab90-139">日付と時刻の関数</span><span class="sxs-lookup"><span data-stu-id="2ab90-139">Date and time functions</span></span>

|<span data-ttu-id="2ab90-140">**Function**</span><span class="sxs-lookup"><span data-stu-id="2ab90-140">**Function**</span></span>|<span data-ttu-id="2ab90-141">**説明**</span><span class="sxs-lookup"><span data-stu-id="2ab90-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2ab90-142">DATE</span><span class="sxs-lookup"><span data-stu-id="2ab90-142">DATE</span></span>](date-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-143">数値を日付の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-143">Converts numbers to a date value.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-144">DATETIME</span><span class="sxs-lookup"><span data-stu-id="2ab90-144">DATETIME</span></span>](datetime-function.md) <br/> | <span data-ttu-id="2ab90-145">文字列を日付と時刻の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-145">Converts a string to a date and time value.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-146">DATEVALUE</span><span class="sxs-lookup"><span data-stu-id="2ab90-146">DATEVALUE</span></span>](datevalue-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-147">文字列を日付の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-147">Converts a string to a date value.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-148">NOW</span><span class="sxs-lookup"><span data-stu-id="2ab90-148">NOW</span></span>](now-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-149">現在のシステムの日付を日付と時刻の値として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-149">Returns the current system date as a date and time value.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-150">TIME</span><span class="sxs-lookup"><span data-stu-id="2ab90-150">TIME</span></span>](time-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-151">数値を時刻の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-151">Converts numbers to a time value.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-152">TIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="2ab90-152">TIMEVALUE</span></span>](timevalue-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-153">文字列を時刻の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-153">Converts a string to a time value.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-154">DAY</span><span class="sxs-lookup"><span data-stu-id="2ab90-154">DAY</span></span>](day-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-155">日付のうち、日を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-155">Returns the day component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-156">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2ab90-156">DAYOFYEAR</span></span>](dayofyear-function.md) <br/> | <span data-ttu-id="2ab90-157">年の何日目かを表す値を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-157">Returns the sequential day of the year in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-158">HOUR</span><span class="sxs-lookup"><span data-stu-id="2ab90-158">HOUR</span></span>](hour-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-159">時刻のうち、時間を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-159">Returns the hours component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-160">MINUTE</span><span class="sxs-lookup"><span data-stu-id="2ab90-160">MINUTE</span></span>](minute-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-161">時刻のうち、分を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-161">Returns the minutes component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-162">MONTH</span><span class="sxs-lookup"><span data-stu-id="2ab90-162">MONTH</span></span>](month-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-163">日付のうち、月を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-163">Returns the month component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-164">SECOND</span><span class="sxs-lookup"><span data-stu-id="2ab90-164">SECOND</span></span>](second-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-165">時刻のうち、秒を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-165">Returns the seconds component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-166">WEEKDAY</span><span class="sxs-lookup"><span data-stu-id="2ab90-166">WEEKDAY</span></span>](weekday-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-167">曜日の番号を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-167">Returns the number of the weekday in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="2ab90-168">YEAR</span><span class="sxs-lookup"><span data-stu-id="2ab90-168">YEAR</span></span>](year-function-visioshapesheet.md) <br/> | <span data-ttu-id="2ab90-169">日付のうち、年を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-169">Returns the year component in a date and time expression.</span></span>  <br/> |
   
## <a name="duration"></a><span data-ttu-id="2ab90-170">期間</span><span class="sxs-lookup"><span data-stu-id="2ab90-170">Duration</span></span>

<span data-ttu-id="2ab90-p104">期間または経過時間を計算する演算を実行できます。期間は、内部的には日数と時間を表す小数部分から成る形式で保存されます。たとえば、1 週間経過、7 日間経過、および 168 時間経過は、すべて内部的には 7.0 として保存されますが、表示には適切な単位で表示されます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-p104">You can perform operations that calculate duration or elapsed time. Duration is stored internally as days and the fraction of a day. For example, 1 elapsed week, 7 elapsed days, and 168 elapsed hours all are stored internally as 7.0, but are displayed with the appropriate units.</span></span>
  
<span data-ttu-id="2ab90-174">Visio は、次の表にある期間の単位を認識します。</span><span class="sxs-lookup"><span data-stu-id="2ab90-174">Visio recognizes the units of duration in the following table.</span></span>
  
|<span data-ttu-id="2ab90-175">**単位**</span><span class="sxs-lookup"><span data-stu-id="2ab90-175">**Unit**</span></span>|<span data-ttu-id="2ab90-176">**略語**</span><span class="sxs-lookup"><span data-stu-id="2ab90-176">**Abbreviation**</span></span>|<span data-ttu-id="2ab90-177">**汎用省略形**</span><span class="sxs-lookup"><span data-stu-id="2ab90-177">**Universal abbreviation**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2ab90-178">経過した日数</span><span class="sxs-lookup"><span data-stu-id="2ab90-178">elapsed day</span></span>  <br/> | <span data-ttu-id="2ab90-179">eday, ed.</span><span class="sxs-lookup"><span data-stu-id="2ab90-179">eday, ed.</span></span>  <br/> | <span data-ttu-id="2ab90-180">ed</span><span class="sxs-lookup"><span data-stu-id="2ab90-180">ed</span></span>  <br/> |
| <span data-ttu-id="2ab90-181">経過した時間</span><span class="sxs-lookup"><span data-stu-id="2ab90-181">elapsed hour</span></span>  <br/> | <span data-ttu-id="2ab90-182">ehour, eh.</span><span class="sxs-lookup"><span data-stu-id="2ab90-182">ehour, eh.</span></span>  <br/> | <span data-ttu-id="2ab90-183">eh</span><span class="sxs-lookup"><span data-stu-id="2ab90-183">eh</span></span>  <br/> |
| <span data-ttu-id="2ab90-184">経過した分数</span><span class="sxs-lookup"><span data-stu-id="2ab90-184">elapsed minute</span></span>  <br/> | <span data-ttu-id="2ab90-185">eminute, em.</span><span class="sxs-lookup"><span data-stu-id="2ab90-185">eminute, em.</span></span>  <br/> | <span data-ttu-id="2ab90-186">em</span><span class="sxs-lookup"><span data-stu-id="2ab90-186">em</span></span>  <br/> |
| <span data-ttu-id="2ab90-187">経過した秒数</span><span class="sxs-lookup"><span data-stu-id="2ab90-187">elapsed second</span></span>  <br/> | <span data-ttu-id="2ab90-188">esecond, es.</span><span class="sxs-lookup"><span data-stu-id="2ab90-188">esecond, es.</span></span>  <br/> | <span data-ttu-id="2ab90-189">es</span><span class="sxs-lookup"><span data-stu-id="2ab90-189">es</span></span>  <br/> |
| <span data-ttu-id="2ab90-190">経過した週数</span><span class="sxs-lookup"><span data-stu-id="2ab90-190">elapsed week</span></span>  <br/> | <span data-ttu-id="2ab90-191">eweek, ew.</span><span class="sxs-lookup"><span data-stu-id="2ab90-191">eweek, ew.</span></span>  <br/> | <span data-ttu-id="2ab90-192">ew</span><span class="sxs-lookup"><span data-stu-id="2ab90-192">ew</span></span>  <br/> |
   
<span data-ttu-id="2ab90-p105">期間に日付と時刻を加えて、新しい日付と時刻を計算できます。日付、時刻、期間を使用して、次の表に示される演算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="2ab90-p105">You can add a date and time to a duration to calculate a new date and time. You can perform the operations listed in this table using dates, times, and durations.</span></span>
  
|<span data-ttu-id="2ab90-195">**入力**</span><span class="sxs-lookup"><span data-stu-id="2ab90-195">**Input**</span></span>|<span data-ttu-id="2ab90-196">**結果**</span><span class="sxs-lookup"><span data-stu-id="2ab90-196">**Result**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2ab90-197">日付-時刻 +/- 期間</span><span class="sxs-lookup"><span data-stu-id="2ab90-197">Date-time +/- duration</span></span>  <br/> | <span data-ttu-id="2ab90-198">日付と時刻の値</span><span class="sxs-lookup"><span data-stu-id="2ab90-198">Date and time value</span></span>  <br/> |
| <span data-ttu-id="2ab90-199">期間 +/- 日付-時刻</span><span class="sxs-lookup"><span data-stu-id="2ab90-199">Duration +/- date-time</span></span>  <br/> | <span data-ttu-id="2ab90-200">日付と時刻の値</span><span class="sxs-lookup"><span data-stu-id="2ab90-200">Date and time value</span></span>  <br/> |
| <span data-ttu-id="2ab90-201">期間 +/- 期間</span><span class="sxs-lookup"><span data-stu-id="2ab90-201">Duration +/- duration</span></span>  <br/> | <span data-ttu-id="2ab90-202">期間の値</span><span class="sxs-lookup"><span data-stu-id="2ab90-202">Duration value</span></span>  <br/> |
| <span data-ttu-id="2ab90-203">日付-時間 + 日付-時間</span><span class="sxs-lookup"><span data-stu-id="2ab90-203">Date-time + date-time</span></span>  <br/> | <span data-ttu-id="2ab90-204">日付と時刻の値</span><span class="sxs-lookup"><span data-stu-id="2ab90-204">Date and time value</span></span>  <br/> |
| <span data-ttu-id="2ab90-205">日付-時間 - 日付-時間</span><span class="sxs-lookup"><span data-stu-id="2ab90-205">Date-time - date-time</span></span>  <br/> | <span data-ttu-id="2ab90-206">期間の値</span><span class="sxs-lookup"><span data-stu-id="2ab90-206">Duration value</span></span>  <br/> |
   

