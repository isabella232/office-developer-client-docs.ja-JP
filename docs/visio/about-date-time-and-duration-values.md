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
description: 日付、時刻、および期間の値を使用して数式での操作を行うことができます。 Microsoft Visio では、単一の値として、日付と時刻の式を評価できます。 日付と時刻の式は、日付や時刻、または日付と時刻を含むセルへの参照として一般的に認識される任意の式です。 これには、文字列と日付と時刻のような数字が含まれから日付と時刻の値が返される関数です。
ms.openlocfilehash: 936055ed6d13b75bd0c42c95564046a76082ec0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804744"
---
# <a name="about-date-time-and-duration-values"></a><span data-ttu-id="7607c-106">日付、時刻、期間の値について</span><span class="sxs-lookup"><span data-stu-id="7607c-106">About Date, Time, and Duration Values</span></span>

<span data-ttu-id="7607c-107">日付、時刻、および期間の値を使用して数式での操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="7607c-107">You can perform operations in formulas using date, time, and duration values.</span></span> <span data-ttu-id="7607c-108">Microsoft Visio では、単一の値として、日付と時刻の式を評価できます。</span><span class="sxs-lookup"><span data-stu-id="7607c-108">In Microsoft Visio, a date and time expression can be evaluated as a single value.</span></span> <span data-ttu-id="7607c-109">日付と時刻の式は、日付や時刻、または日付と時刻を含むセルへの参照として一般的に認識される任意の式です。</span><span class="sxs-lookup"><span data-stu-id="7607c-109">A date and time expression is any expression commonly recognized as a date and/or time or a reference to a cell containing a date and/or time.</span></span> <span data-ttu-id="7607c-110">これには、文字列と日付と時刻のような数字が含まれから日付と時刻の値が返される関数です。</span><span class="sxs-lookup"><span data-stu-id="7607c-110">This includes strings and numbers that look like a date and time, and date and time values returned from functions.</span></span>
  
<span data-ttu-id="7607c-111">Visio での日付と時刻の値は、64 ビットの浮動小数点数として内部的に格納されます。</span><span class="sxs-lookup"><span data-stu-id="7607c-111">Date and time values in Visio are stored internally as a 64-bit floating point number.</span></span> <span data-ttu-id="7607c-112">小数点の左側に値は、1899 年 12 月 30 日以降の日数を表します。</span><span class="sxs-lookup"><span data-stu-id="7607c-112">The value to the left of the decimal represents the number of days since December 30, 1899.</span></span> <span data-ttu-id="7607c-113">小数点の右側の値は、午前 0 時から 1 日の端数を表します。</span><span class="sxs-lookup"><span data-stu-id="7607c-113">The value to the right of the decimal represents the fraction of a day since midnight.</span></span> <span data-ttu-id="7607c-114">正午は.5 と表されます。</span><span class="sxs-lookup"><span data-stu-id="7607c-114">Noon is represented by .5.</span></span>
  
<span data-ttu-id="7607c-115">単一の定数としてではなく、式で日付と時刻を使用するには、日付と時刻の値であることを識別するために適切な関数を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7607c-115">To use dates and times within an expression (rather than as a single constant), you must use the appropriate function to identify them as date and time values.</span></span>
  
## <a name="valid-dates"></a><span data-ttu-id="7607c-116">有効な日付</span><span class="sxs-lookup"><span data-stu-id="7607c-116">Valid dates</span></span>

||||
|:-----|:-----|:-----|
| <span data-ttu-id="7607c-117">「2/28」</span><span class="sxs-lookup"><span data-stu-id="7607c-117">"2/28"</span></span>  <br/> | <span data-ttu-id="7607c-118">「2/28/99」</span><span class="sxs-lookup"><span data-stu-id="7607c-118">"2/28/99"</span></span>  <br/> | <span data-ttu-id="7607c-119">「1999/2/28」</span><span class="sxs-lookup"><span data-stu-id="7607c-119">"2/28/1999"</span></span>  <br/> |
| <span data-ttu-id="7607c-120">「2-28」</span><span class="sxs-lookup"><span data-stu-id="7607c-120">"2-28"</span></span>  <br/> | <span data-ttu-id="7607c-121">「2-28-99」</span><span class="sxs-lookup"><span data-stu-id="7607c-121">"2-28-99"</span></span>  <br/> | <span data-ttu-id="7607c-122">「1999/2-28」</span><span class="sxs-lookup"><span data-stu-id="7607c-122">"2-28/1999"</span></span>  <br/> |
| <span data-ttu-id="7607c-123">「6 年 3 月 99」</span><span class="sxs-lookup"><span data-stu-id="7607c-123">"6 Mar 99"</span></span>  <br/> | <span data-ttu-id="7607c-124">「6 年 3 月」</span><span class="sxs-lookup"><span data-stu-id="7607c-124">"6 Mar"</span></span>  <br/> | <span data-ttu-id="7607c-125">「6 年 3 月 99」</span><span class="sxs-lookup"><span data-stu-id="7607c-125">"6 Mar 99"</span></span>  <br/> |
| <span data-ttu-id="7607c-126">「1 年 1 月 99」</span><span class="sxs-lookup"><span data-stu-id="7607c-126">"1 January 99"</span></span>  <br/> | <span data-ttu-id="7607c-127">「99 年 1 月 1日」</span><span class="sxs-lookup"><span data-stu-id="7607c-127">"Jan 1, 99"</span></span>  <br/> | <span data-ttu-id="7607c-128">「1999 年 1 月 1日日」</span><span class="sxs-lookup"><span data-stu-id="7607c-128">"Jan 1, 1999"</span></span>  <br/> |
| <span data-ttu-id="7607c-129">「1 月 00」</span><span class="sxs-lookup"><span data-stu-id="7607c-129">"Jan 00"</span></span>  <br/> | <span data-ttu-id="7607c-130">」、2000 年 1 月「</span><span class="sxs-lookup"><span data-stu-id="7607c-130">"January, 2000"</span></span>  <br/> | <span data-ttu-id="7607c-131">「00 年 1 月 1日」</span><span class="sxs-lookup"><span data-stu-id="7607c-131">"Jan 1, 00"</span></span>  <br/> |
   
## <a name="valid-times"></a><span data-ttu-id="7607c-132">有効な時刻</span><span class="sxs-lookup"><span data-stu-id="7607c-132">Valid times</span></span>

||||
|:-----|:-----|:-----|
| <span data-ttu-id="7607c-133">[3:45"</span><span class="sxs-lookup"><span data-stu-id="7607c-133">"3:45"</span></span>  <br/> | <span data-ttu-id="7607c-134">"3: 45:27]</span><span class="sxs-lookup"><span data-stu-id="7607c-134">"3:45:27"</span></span>  <br/> | <span data-ttu-id="7607c-135">"7 a"</span><span class="sxs-lookup"><span data-stu-id="7607c-135">"7a"</span></span>  <br/> |
| <span data-ttu-id="7607c-136">7 am</span><span class="sxs-lookup"><span data-stu-id="7607c-136">"7 am"</span></span>  <br/> | <span data-ttu-id="7607c-137">7 p</span><span class="sxs-lookup"><span data-stu-id="7607c-137">"7 p"</span></span>  <br/> | <span data-ttu-id="7607c-138">"7時 30分 PM"</span><span class="sxs-lookup"><span data-stu-id="7607c-138">"7:30 PM"</span></span>  <br/> |
   
## <a name="date-and-time-functions"></a><span data-ttu-id="7607c-139">日付/時刻関数</span><span class="sxs-lookup"><span data-stu-id="7607c-139">Date and time functions</span></span>

|<span data-ttu-id="7607c-140">**関数**</span><span class="sxs-lookup"><span data-stu-id="7607c-140">**Function**</span></span>|<span data-ttu-id="7607c-141">**説明**</span><span class="sxs-lookup"><span data-stu-id="7607c-141">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7607c-142">DATE</span><span class="sxs-lookup"><span data-stu-id="7607c-142">DATE</span></span>](date-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-143">数値を日付値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7607c-143">Converts numbers to a date value.</span></span>  <br/> |
|[<span data-ttu-id="7607c-144">DATETIME</span><span class="sxs-lookup"><span data-stu-id="7607c-144">DATETIME</span></span>](datetime-function.md) <br/> | <span data-ttu-id="7607c-145">文字列を日付と時刻の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7607c-145">Converts a string to a date and time value.</span></span>  <br/> |
|[<span data-ttu-id="7607c-146">DATEVALUE 関数</span><span class="sxs-lookup"><span data-stu-id="7607c-146">DATEVALUE</span></span>](datevalue-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-147">文字列を日付値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7607c-147">Converts a string to a date value.</span></span>  <br/> |
|[<span data-ttu-id="7607c-148">NOW</span><span class="sxs-lookup"><span data-stu-id="7607c-148">NOW</span></span>](now-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-149">日付と時刻の値として現在のシステム日付を返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-149">Returns the current system date as a date and time value.</span></span>  <br/> |
|[<span data-ttu-id="7607c-150">時間</span><span class="sxs-lookup"><span data-stu-id="7607c-150">TIME</span></span>](time-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-151">数値を時刻の値に変換します。</span><span class="sxs-lookup"><span data-stu-id="7607c-151">Converts numbers to a time value.</span></span>  <br/> |
|[<span data-ttu-id="7607c-152">TIMEVALUE</span><span class="sxs-lookup"><span data-stu-id="7607c-152">TIMEVALUE</span></span>](timevalue-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-153">時刻値を文字列に変換します。</span><span class="sxs-lookup"><span data-stu-id="7607c-153">Converts a string to a time value.</span></span>  <br/> |
|[<span data-ttu-id="7607c-154">1 日</span><span class="sxs-lookup"><span data-stu-id="7607c-154">DAY</span></span>](day-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-155">日を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-155">Returns the day component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-156">DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="7607c-156">DAYOFYEAR</span></span>](dayofyear-function.md) <br/> | <span data-ttu-id="7607c-157">日付と時刻の式では、1 年の何日目を返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-157">Returns the sequential day of the year in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-158">1 時間</span><span class="sxs-lookup"><span data-stu-id="7607c-158">HOUR</span></span>](hour-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-159">時間を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-159">Returns the hours component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-160">1 分</span><span class="sxs-lookup"><span data-stu-id="7607c-160">MINUTE</span></span>](minute-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-161">分を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-161">Returns the minutes component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-162">月</span><span class="sxs-lookup"><span data-stu-id="7607c-162">MONTH</span></span>](month-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-163">月を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-163">Returns the month component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-164">1 秒</span><span class="sxs-lookup"><span data-stu-id="7607c-164">SECOND</span></span>](second-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-165">秒数を返す、日付と時刻の式のコンポーネントです。</span><span class="sxs-lookup"><span data-stu-id="7607c-165">Returns the seconds component in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-166">曜日</span><span class="sxs-lookup"><span data-stu-id="7607c-166">WEEKDAY</span></span>](weekday-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-167">日付と時刻の式では、曜日の番号を返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-167">Returns the number of the weekday in a date and time expression.</span></span>  <br/> |
|[<span data-ttu-id="7607c-168">年</span><span class="sxs-lookup"><span data-stu-id="7607c-168">YEAR</span></span>](year-function-visioshapesheet.md) <br/> | <span data-ttu-id="7607c-169">年を日付と時刻の式として返します。</span><span class="sxs-lookup"><span data-stu-id="7607c-169">Returns the year component in a date and time expression.</span></span>  <br/> |
   
## <a name="duration"></a><span data-ttu-id="7607c-170">Duration</span><span class="sxs-lookup"><span data-stu-id="7607c-170">Duration</span></span>

<span data-ttu-id="7607c-p104">期間または経過時間を計算する演算を実行できます。期間は、内部的には日数と時間を表す小数部分から成る形式で保存されます。たとえば、1 週間経過、7 日間経過、および 168 時間経過は、すべて内部的には 7.0 として保存されますが、表示には適切な単位で表示されます。</span><span class="sxs-lookup"><span data-stu-id="7607c-p104">You can perform operations that calculate duration or elapsed time. Duration is stored internally as days and the fraction of a day. For example, 1 elapsed week, 7 elapsed days, and 168 elapsed hours all are stored internally as 7.0, but are displayed with the appropriate units.</span></span>
  
<span data-ttu-id="7607c-174">Visio で認識される期間の単位は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="7607c-174">Visio recognizes the units of duration in the following table.</span></span>
  
|<span data-ttu-id="7607c-175">**Unit**</span><span class="sxs-lookup"><span data-stu-id="7607c-175">**Unit**</span></span>|<span data-ttu-id="7607c-176">**Abbreviation**</span><span class="sxs-lookup"><span data-stu-id="7607c-176">**Abbreviation**</span></span>|<span data-ttu-id="7607c-177">**汎用省略形**</span><span class="sxs-lookup"><span data-stu-id="7607c-177">**Universal abbreviation**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7607c-178">経過した日数</span><span class="sxs-lookup"><span data-stu-id="7607c-178">elapsed day</span></span>  <br/> | <span data-ttu-id="7607c-179">eday、ed。</span><span class="sxs-lookup"><span data-stu-id="7607c-179">eday, ed.</span></span>  <br/> | <span data-ttu-id="7607c-180">ed</span><span class="sxs-lookup"><span data-stu-id="7607c-180">ed</span></span>  <br/> |
| <span data-ttu-id="7607c-181">経過時間</span><span class="sxs-lookup"><span data-stu-id="7607c-181">elapsed hour</span></span>  <br/> | <span data-ttu-id="7607c-182">ehour、んです。</span><span class="sxs-lookup"><span data-stu-id="7607c-182">ehour, eh.</span></span>  <br/> | <span data-ttu-id="7607c-183">eh</span><span class="sxs-lookup"><span data-stu-id="7607c-183">eh</span></span>  <br/> |
| <span data-ttu-id="7607c-184">経過した分数</span><span class="sxs-lookup"><span data-stu-id="7607c-184">elapsed minute</span></span>  <br/> | <span data-ttu-id="7607c-185">eminute、em。</span><span class="sxs-lookup"><span data-stu-id="7607c-185">eminute, em.</span></span>  <br/> | <span data-ttu-id="7607c-186">em</span><span class="sxs-lookup"><span data-stu-id="7607c-186">em</span></span>  <br/> |
| <span data-ttu-id="7607c-187">経過した秒数</span><span class="sxs-lookup"><span data-stu-id="7607c-187">elapsed second</span></span>  <br/> | <span data-ttu-id="7607c-188">esecond、es です。</span><span class="sxs-lookup"><span data-stu-id="7607c-188">esecond, es.</span></span>  <br/> | <span data-ttu-id="7607c-189">es</span><span class="sxs-lookup"><span data-stu-id="7607c-189">es</span></span>  <br/> |
| <span data-ttu-id="7607c-190">経過した週数</span><span class="sxs-lookup"><span data-stu-id="7607c-190">elapsed week</span></span>  <br/> | <span data-ttu-id="7607c-191">eweek、ew。</span><span class="sxs-lookup"><span data-stu-id="7607c-191">eweek, ew.</span></span>  <br/> | <span data-ttu-id="7607c-192">ew</span><span class="sxs-lookup"><span data-stu-id="7607c-192">ew</span></span>  <br/> |
   
<span data-ttu-id="7607c-p105">期間に日付と時刻を加えて、新しい日付と時刻を計算できます。日付、時刻、期間を使用して、次の表に示される演算を実行できます。</span><span class="sxs-lookup"><span data-stu-id="7607c-p105">You can add a date and time to a duration to calculate a new date and time. You can perform the operations listed in this table using dates, times, and durations.</span></span>
  
|<span data-ttu-id="7607c-195">**Input**</span><span class="sxs-lookup"><span data-stu-id="7607c-195">**Input**</span></span>|<span data-ttu-id="7607c-196">**結果**</span><span class="sxs-lookup"><span data-stu-id="7607c-196">**Result**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7607c-197">日付と時刻の期間の +/-</span><span class="sxs-lookup"><span data-stu-id="7607c-197">Date-time +/- duration</span></span>  <br/> | <span data-ttu-id="7607c-198">日付と時刻の値</span><span class="sxs-lookup"><span data-stu-id="7607c-198">Date and time value</span></span>  <br/> |
| <span data-ttu-id="7607c-199">+/-の日付と時刻の期間</span><span class="sxs-lookup"><span data-stu-id="7607c-199">Duration +/- date-time</span></span>  <br/> | <span data-ttu-id="7607c-200">日付と時刻の値</span><span class="sxs-lookup"><span data-stu-id="7607c-200">Date and time value</span></span>  <br/> |
| <span data-ttu-id="7607c-201">+/-の期間の期間</span><span class="sxs-lookup"><span data-stu-id="7607c-201">Duration +/- duration</span></span>  <br/> | <span data-ttu-id="7607c-202">期間の値</span><span class="sxs-lookup"><span data-stu-id="7607c-202">Duration value</span></span>  <br/> |
| <span data-ttu-id="7607c-203">日付と時刻と日付と時刻</span><span class="sxs-lookup"><span data-stu-id="7607c-203">Date-time + date-time</span></span>  <br/> | <span data-ttu-id="7607c-204">日付と時刻の値</span><span class="sxs-lookup"><span data-stu-id="7607c-204">Date and time value</span></span>  <br/> |
| <span data-ttu-id="7607c-205">日付と時刻 - 日付と時刻</span><span class="sxs-lookup"><span data-stu-id="7607c-205">Date-time - date-time</span></span>  <br/> | <span data-ttu-id="7607c-206">期間の値</span><span class="sxs-lookup"><span data-stu-id="7607c-206">Duration value</span></span>  <br/> |
   

