---
title: 週単位パターンの定期的な予定を作成する
TOCTitle: Create a recurring appointment that has a weekly pattern
ms:assetid: 20b46b26-e278-451b-9e35-36683205d164
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184595(v=office.15)
ms:contentKeyID: 55119810
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b326ad23f8cbe47e5141775eacdd2bc9302db3cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359172"
---
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a><span data-ttu-id="31eb2-102">週単位パターンの定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="31eb2-102">Create a recurring appointment that has a weekly pattern</span></span>

<span data-ttu-id="31eb2-103">この例では、週単位パターンの定期的な予定 (たとえば、毎週の月曜日と水曜日と金曜日に発生する予定) を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="31eb2-103">This example shows how to create a recurring appointment that has a weekly pattern (for example, an appointment that occurs every Monday, Wednesday, and Friday).</span></span>

## <a name="example"></a><span data-ttu-id="31eb2-104">例</span><span class="sxs-lookup"><span data-stu-id="31eb2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="31eb2-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="31eb2-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="31eb2-106">新しい定期的な予定を作成する場合、定期的なパターンは予定の作成時に指定した時間に基づきます。</span><span class="sxs-lookup"><span data-stu-id="31eb2-106">When you create a new recurring appointment, the recurrence pattern is based on the time you specify when you create the appointment.</span></span> <span data-ttu-id="31eb2-107">たとえば、毎日繰り返される予定を午後 1:00 に作成した場合、その予定は毎日午後 1:00 にだけ繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="31eb2-107">For example, if you create an appointment that recurs daily at 1:00 PM, the appointment will recur only at 1:00 PM on a daily basis.</span></span> <span data-ttu-id="31eb2-108">予定の定期的なパターンを変更するには、予定の [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトのプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="31eb2-108">To change the recurrence pattern of an appointment, set the properties of the appointment’s [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="31eb2-109">RecurrencePattern オブジェクトの [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) プロパティは、RecurrencePattern のその他のプロパティよりも先に設定してください。</span><span class="sxs-lookup"><span data-stu-id="31eb2-109">Set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the RecurrencePattern object before setting other RecurrencePattern properties.</span></span> <span data-ttu-id="31eb2-110">次の表は、特定の RecurrenceType ([OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) 列挙型で指定) に対して有効な RecurrencePattern のプロパティを示しています。</span><span class="sxs-lookup"><span data-stu-id="31eb2-110">The following table shows valid RecurrencePattern properties for a given RecurrenceType (specified by the [OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) enumeration).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="31eb2-111">OlRecurrenceType の値</span><span class="sxs-lookup"><span data-stu-id="31eb2-111">OlRecurrenceType value</span></span></p></th>
<th><p><span data-ttu-id="31eb2-112">有効な RecurrencePattern のプロパティ</span><span class="sxs-lookup"><span data-stu-id="31eb2-112">Valid RecurrencePattern properties</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="31eb2-113">olRecursDaily</span><span class="sxs-lookup"><span data-stu-id="31eb2-113">olRecursDaily</span></span></p></td>
<td><p><span data-ttu-id="31eb2-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>、<a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>、<a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>、<a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>、<a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>、<a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>、<a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>、<a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span><span class="sxs-lookup"><span data-stu-id="31eb2-114"><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>, <a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>, <a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>, <a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>, <a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>, <a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>, <a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>, <a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31eb2-115">olRecursWeekly</span><span class="sxs-lookup"><span data-stu-id="31eb2-115">olRecursWeekly</span></span></p></td>
<td><p><span data-ttu-id="31eb2-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>、Duration、EndTime、Interval、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</span><span class="sxs-lookup"><span data-stu-id="31eb2-116"><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31eb2-117">olRecursMonthly</span><span class="sxs-lookup"><span data-stu-id="31eb2-117">olRecursMonthly</span></span></p></td>
<td><p><span data-ttu-id="31eb2-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>、Duration、EndTime、Interval、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</span><span class="sxs-lookup"><span data-stu-id="31eb2-118"><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>, Duration, EndTime, Interval, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31eb2-119">olRecursMonthNth</span><span class="sxs-lookup"><span data-stu-id="31eb2-119">olRecursMonthNth</span></span></p></td>
<td><p><span data-ttu-id="31eb2-120">DayOfWeekMask、Duration、EndTime、Interval、<a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</span><span class="sxs-lookup"><span data-stu-id="31eb2-120">DayOfWeekMask, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="31eb2-121">olRecursYearly</span><span class="sxs-lookup"><span data-stu-id="31eb2-121">olRecursYearly</span></span></p></td>
<td><p><span data-ttu-id="31eb2-122">DayOfMonth、Duration、EndTime、Interval、<a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</span><span class="sxs-lookup"><span data-stu-id="31eb2-122">DayOfMonth, Duration, EndTime, Interval, <a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="31eb2-123">olRecursYearNth</span><span class="sxs-lookup"><span data-stu-id="31eb2-123">olRecursYearNth</span></span></p></td>
<td><p><span data-ttu-id="31eb2-124">DayOfWeekMask、Duration、EndTime、Interval、Instance、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</span><span class="sxs-lookup"><span data-stu-id="31eb2-124">DayOfWeekMask, Duration, EndTime, Interval, Instance, NoEndDate, Occurrences, PatternStartDate, PatternEndDate, StartTime</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31eb2-125">定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31eb2-125">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="31eb2-126">この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。</span><span class="sxs-lookup"><span data-stu-id="31eb2-126">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="31eb2-127">Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。</span><span class="sxs-lookup"><span data-stu-id="31eb2-127">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="31eb2-128">C\# では、そのオブジェクトのメモリを明示的に解放します。</span><span class="sxs-lookup"><span data-stu-id="31eb2-128">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="31eb2-p103">参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="31eb2-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="31eb2-131">次のコード例では、RecurringAppointmentEveryMondayWednesdayFriday で [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成し、新しく作成した予定の RecurrencePattern オブジェクト取得するために [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) を呼び出しています。</span><span class="sxs-lookup"><span data-stu-id="31eb2-131">In the following code example, RecurringAppointmentEveryMondayWednesdayFriday creates an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object, and then calls [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) to get the newly created appointment’s RecurrencePattern object.</span></span> <span data-ttu-id="31eb2-132">その後、RecurringAppointmentEveryMondayWednesdayFriday では、RecurrenceType、DayOfWeekMask、PatternStartDate、PatternEndDate、Duration、StartTime、EndTime、および Subject の各プロパティを設定し、予定を保存して、最終的に「毎週月曜、水曜、金曜に発生: 有効期間 2006/7/10 から 2006/8/25: 午後 2:00 から午後 3:00 まで」のパターンで予定を表示します。</span><span class="sxs-lookup"><span data-stu-id="31eb2-132">RecurringAppointmentEveryMondayWednesdayFriday then sets the RecurrenceType, DayOfWeekMask, PatternStartDate, PatternEndDate, Duration, StartTime, EndTime, and Subject properties, saves the appointment, and finally displays the appointment with the pattern "Occurs every Monday, Wednesday, and Friday effective 7/10/2006 until 8/25/2006 from 2:00 PM to 3:00 PM."</span></span>

<span data-ttu-id="31eb2-133">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="31eb2-133">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="31eb2-134">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="31eb2-134">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="31eb2-135">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="31eb2-135">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringAppointmentEveryMondayWednesdayFriday()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring Appointment DaysOfWeekMask Example";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursWeekly;
    // Logical OR for DayOfWeekMask creates pattern
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday |
        Outlook.OlDaysOfWeek.olWednesday |
        Outlook.OlDaysOfWeek.olFriday;
    pattern.PatternStartDate = DateTime.Parse("7/10/2006");
    pattern.PatternEndDate = DateTime.Parse("8/25/2006");
    pattern.Duration = 60;
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("3:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="31eb2-136">関連項目</span><span class="sxs-lookup"><span data-stu-id="31eb2-136">See also</span></span>

- [<span data-ttu-id="31eb2-137">予定</span><span class="sxs-lookup"><span data-stu-id="31eb2-137">Appointments</span></span>](appointments.md)

