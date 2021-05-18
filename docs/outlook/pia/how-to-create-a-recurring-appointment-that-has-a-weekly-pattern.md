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
# <a name="create-a-recurring-appointment-that-has-a-weekly-pattern"></a>週単位パターンの定期的な予定を作成する

この例では、週単位パターンの定期的な予定 (たとえば、毎週の月曜日と水曜日と金曜日に発生する予定) を作成する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


新しい定期的な予定を作成する場合、定期的なパターンは予定の作成時に指定した時間に基づきます。 たとえば、毎日繰り返される予定を午後 1:00 に作成した場合、その予定は毎日午後 1:00 にだけ繰り返されます。 予定の定期的なパターンを変更するには、予定の [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトのプロパティを設定します。 RecurrencePattern オブジェクトの [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) プロパティは、RecurrencePattern のその他のプロパティよりも先に設定してください。 次の表は、特定の RecurrenceType ([OlRecurrenceType](https://msdn.microsoft.com/library/bb647129\(v=office.15\)) 列挙型で指定) に対して有効な RecurrencePattern のプロパティを示しています。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>OlRecurrenceType の値</p></th>
<th><p>有効な RecurrencePattern のプロパティ</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>olRecursDaily</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb644889(v=office.15)">Duration</a>、<a href="https://msdn.microsoft.com/library/bb644544(v=office.15)">EndTime</a>、<a href="https://msdn.microsoft.com/library/bb624287(v=office.15)">Interval</a>、<a href="https://msdn.microsoft.com/library/bb646849(v=office.15)">NoEndDate</a>、<a href="https://msdn.microsoft.com/library/bb611303(v=office.15)">Occurrences</a>、<a href="https://msdn.microsoft.com/library/bb624492(v=office.15)">PatternStartDate</a>、<a href="https://msdn.microsoft.com/library/bb609279(v=office.15)">PatternEndDate</a>、<a href="https://msdn.microsoft.com/library/bb646324(v=office.15)">StartTime</a></p></td>
</tr>
<tr class="even">
<td><p>olRecursWeekly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb609163(v=office.15)">DayOfWeekMask</a>、Duration、EndTime、Interval、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursMonthly</p></td>
<td><p><a href="https://msdn.microsoft.com/library/bb622604(v=office.15)">DayOfMonth</a>、Duration、EndTime、Interval、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursMonthNth</p></td>
<td><p>DayOfWeekMask、Duration、EndTime、Interval、<a href="https://msdn.microsoft.com/library/bb645269(v=office.15)">Instance</a>、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</p></td>
</tr>
<tr class="odd">
<td><p>olRecursYearly</p></td>
<td><p>DayOfMonth、Duration、EndTime、Interval、<a href="https://msdn.microsoft.com/library/bb610515(v=office.15)">MonthOfYear</a>、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</p></td>
</tr>
<tr class="even">
<td><p>olRecursYearNth</p></td>
<td><p>DayOfWeekMask、Duration、EndTime、Interval、Instance、NoEndDate、Occurrences、PatternStartDate、PatternEndDate、StartTime</p></td>
</tr>
</tbody>
</table>


定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。 この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。 Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。 C\# では、そのオブジェクトのメモリを明示的に解放します。

参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。

次のコード例では、RecurringAppointmentEveryMondayWednesdayFriday で [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成し、新しく作成した予定の RecurrencePattern オブジェクト取得するために [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) を呼び出しています。 その後、RecurringAppointmentEveryMondayWednesdayFriday では、RecurrenceType、DayOfWeekMask、PatternStartDate、PatternEndDate、Duration、StartTime、EndTime、および Subject の各プロパティを設定し、予定を保存して、最終的に「毎週月曜、水曜、金曜に発生: 有効期間 2006/7/10 から 2006/8/25: 午後 2:00 から午後 3:00 まで」のパターンで予定を表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

