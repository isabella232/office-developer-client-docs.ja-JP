---
title: YearNth パターンの年単位の定期的な予定を作成する
TOCTitle: Create an annual recurring appointment that uses a YearNth pattern
ms:assetid: 5fb2ad0b-248c-417d-8868-52e0550d970f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184611(v=office.15)
ms:contentKeyID: 55119811
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fd4c0eecca8e04a7953c5f9230082235e46e274e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623741"
---
# <a name="create-an-annual-recurring-appointment-that-uses-a-yearnth-pattern"></a>YearNth パターンの年単位の定期的な予定を作成する

この例では、6 月の第 1 月曜日など、毎年 1 回の特定の曜日を指定した定期的な予定を作成する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

毎年特定の月の特定の曜日 (6 月の第 1 月曜日など) に反復される定期的な予定を作成するには、"YearNth" の定期的なパターンを使用する必要があります。 YearNth のパターンを設定するには、まず、[RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトの [RecurrenceType](https://msdn.microsoft.com/library/bb623463\(v=office.15\)) プロパティを olRecursYearNth に設定する必要があります。 次に、 [DayOfWeekMask](https://msdn.microsoft.com/library/bb609163\(v=office.15\)) プロパティをその予定が反復される曜日に設定し、 [Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\)) プロパティを毎年の指定月の何番目の曜日か ("第 3" 火曜日など) を示すように設定します。

定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。 この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。 Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。 C\# では、そのオブジェクトのメモリを明示的に解放します。

参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。

次のコード例の RecurringYearNthAppointment では、YearNth の定期的なパターンを持つ予定を作成します。 RecurringYearNthAppointment では、まず、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成することで定期的な予定を作成します。 次に、[GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) メソッドを使用して、予定の定期的なパターンを取得します。 その後、RecurrencePattern のプロパティ RecurrenceType、DayOfWeekMask、[MonthOfYear](https://msdn.microsoft.com/library/bb610515\(v=office.15\))、[Instance](https://msdn.microsoft.com/library/bb645269\(v=office.15\))、[Occurrences](https://msdn.microsoft.com/library/bb611303\(v=office.15\))、[Duration](https://msdn.microsoft.com/library/bb644889\(v=office.15\))、[PatternStartDate](https://msdn.microsoft.com/library/bb624492\(v=office.15\))、[StartTime](https://msdn.microsoft.com/library/bb646324\(v=office.15\))、および [EndTime](https://msdn.microsoft.com/library/bb644544\(v=office.15\)) を設定します。 MonthOfYear プロパティは、1 から 12 の数値を受け入れます。それぞれの数値が、対応する月を表します。 プロパティの設定後、RecurringYearNthAppointment では、予定を保存して、その予定を「6 月の最初の月曜日に発生、2007 年 6 月 1 日から 2016 年 6 月 6 日まで有効、午後 2 時 00 分から午後 5 時 00 分まで」のパターンで表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

