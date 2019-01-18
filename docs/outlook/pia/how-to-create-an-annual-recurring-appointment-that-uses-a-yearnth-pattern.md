---
title: YearNth パターンの年単位の定期的な予定を作成する
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9fc50166674ee7b9699ef8e29c5ff1e54db705ad
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712156"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a><span data-ttu-id="ae9c7-102">YearNth パターンの年単位の定期的な予定を作成する</span><span class="sxs-lookup"><span data-stu-id="ae9c7-102">Create an annual recurring appointment that uses a YearNth pattern</span></span>

<span data-ttu-id="ae9c7-103">この例では、6 月の第 1 月曜日など、毎年 1 回の特定の曜日を指定した定期的な予定を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-103">This example shows how to create an appointment for which the annual recurrence pattern is a specific day such as the first Monday in June.</span></span>

## <a name="example"></a><span data-ttu-id="ae9c7-104">例</span><span class="sxs-lookup"><span data-stu-id="ae9c7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ae9c7-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ae9c7-106">毎年特定の月の特定の曜日 (6 月の第 1 月曜日など) に反復される定期的な予定を作成するには、"YearNth" の定期的なパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-106">If you want to create an annual appointment that recurs on a specific day of the week during a specific month (for example, the first Monday in June), you must use YearNth recurrences.</span></span> <span data-ttu-id="ae9c7-107">YearNth のパターンを設定するには、まず、[RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトの [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) プロパティを olRecursYearNth に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-107">To set a YearNth recurrence, you must first set the [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) property of the [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object to olRecursYearNth.</span></span> <span data-ttu-id="ae9c7-108">次に、 [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) プロパティをその予定が反復される曜日に設定し、 [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) プロパティを毎年の指定月の何番目の曜日か ("第 3" 火曜日など) を示すように設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-108">Then set the [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) property to specify on which day of the week the appointment should recur, and the [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) property to specify the Nth occurrence of the specified day of the week (for example, the third Tuesday) during a specified month for the yearly pattern.</span></span>

<span data-ttu-id="ae9c7-109">定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-109">When you work with recurring appointment items, you should release any prior references, obtain new references to the recurring appointment item before you access or modify the item, and release these references as soon as you are finished and have saved the changes.</span></span> <span data-ttu-id="ae9c7-110">この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-110">This practice applies to the recurring **AppointmentItem** object, and any [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) or [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) object.</span></span> <span data-ttu-id="ae9c7-111">Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-111">To release a reference in Visual Basic, set that existing object to Nothing.</span></span> <span data-ttu-id="ae9c7-112">C\# では、そのオブジェクトのメモリを明示的に解放します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-112">In C\#, explicitly release the memory for that object.</span></span>

<span data-ttu-id="ae9c7-p103">参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-p103">Note that even after you release your reference and attempt to obtain a new reference, if there is still an active reference (held by another add-in or Outlook) to one of the above objects, your new reference will still point to an out-of-date copy of the object. Therefore, it is important that you release your references as soon as you are finished with the recurring appointment.</span></span>

<span data-ttu-id="ae9c7-115">次のコード例の RecurringYearNthAppointment では、YearNth の定期的なパターンを持つ予定を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-115">In the following code example, RecurringYearNthAppointment creates an appointment that has a YearNth recurrence pattern.</span></span> <span data-ttu-id="ae9c7-116">RecurringYearNthAppointment では、まず、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成することで定期的な予定を作成します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-116">RecurringYearNthAppointment first creates a recurring appointment by creating an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span> <span data-ttu-id="ae9c7-117">次に、[GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) メソッドを使用して、予定の定期的なパターンを取得します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-117">Next, it gets the appointment’s recurrence pattern by using the [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) method.</span></span> <span data-ttu-id="ae9c7-118">その後、RecurrencePattern のプロパティ RecurrenceType、DayOfWeekMask、[MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\))、[Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\))、[Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\))、[Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\))、[PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\))、[StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\))、および [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)) を設定します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-118">It then sets the following RecurrencePattern properties: RecurrenceType, DayOfWeekMask, [MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\)), [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)), [Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\)), [Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\)), [PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\)), [StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\)), and [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)).</span></span> <span data-ttu-id="ae9c7-119">MonthOfYear プロパティは、1 から 12 の数値を受け入れます。それぞれの数値が、対応する月を表します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-119">The MonthOfYear property can take a numerical value of 1 through 12, where each number represents the corresponding month.</span></span> <span data-ttu-id="ae9c7-120">プロパティの設定後、RecurringYearNthAppointment では、予定を保存して、その予定を「6 月の最初の月曜日に発生、2007 年 6 月 1 日から 2016 年 6 月 6 日まで有効、午後 2 時 00 分から午後 5 時 00 分まで」のパターンで表示します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-120">Once the properties are set, RecurringYearNthAppointment saves the appointment, and then displays it with the pattern "Occurs the first Monday of June effective 6/1/2007 until 6/6/2016 from 2:00 PM to 5:00 PM."</span></span>

<span data-ttu-id="ae9c7-121">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ae9c7-122">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-122">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ae9c7-123">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ae9c7-123">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void RecurringYearNthAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Recurring YearNth Appointment";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    pattern.RecurrenceType = Outlook.OlRecurrenceType.olRecursYearNth;
    pattern.DayOfWeekMask = Outlook.OlDaysOfWeek.olMonday;
    pattern.MonthOfYear = 6;
    pattern.Instance = 1;
    pattern.Occurrences = 10;
    pattern.Duration = 180;
    pattern.PatternStartDate = DateTime.Parse("6/1/2007");
    pattern.StartTime = DateTime.Parse("2:00:00 PM");
    pattern.EndTime = DateTime.Parse("5:00:00 PM");
    appt.Save();
    appt.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="ae9c7-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="ae9c7-124">See also</span></span>

- [<span data-ttu-id="ae9c7-125">予定</span><span class="sxs-lookup"><span data-stu-id="ae9c7-125">Appointments</span></span>](appointments.md)

