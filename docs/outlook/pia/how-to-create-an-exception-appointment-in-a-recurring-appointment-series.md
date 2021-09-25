---
title: 定期的な一連の予定に例外的な予定を作成する
TOCTitle: Create an exception appointment in a recurring appointment series
ms:assetid: b7cd0975-4f44-453a-b878-ec55feeedc4e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184635(v=office.15)
ms:contentKeyID: 55119813
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: ed3936c5acef1d4dc9526588f7322ac759f5db25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616370"
---
# <a name="create-an-exception-appointment-in-a-recurring-appointment-series"></a>定期的な一連の予定に例外的な予定を作成する

この例では、[Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトを使用して、予定に対する標準の定期的なパターンの例外を作成します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

定期的な予定の 1 つの予定のインスタンスを削除または変更すると、Outlook によって [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトが作成されます。 Exception オブジェクトを使用すると、標準の定期的なパターンに例外を作成できます。 オブジェクトのプロパティには、予定のインスタンスに加えられた変更が格納されています。 [Exceptions](https://msdn.microsoft.com/library/bb647601\(v=office.15\)) コレクションには、定期的な予定の Exception オブジェクトがすべて収容されています。さらに、このコレクションは、予定の [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトに関連付けられています。

定期的な予定の元の定期的なパターンに対する例外を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを取得するには、Exception の [AppointmentItem](https://msdn.microsoft.com/library/bb645648\(v=office.15\)) プロパティを使用します。 返された AppointmentItem のメソッドとプロパティを使用すると、予定の例外のプロパティを設定できます。

定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。 この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。 Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。 C\# では、そのオブジェクトのメモリを明示的に解放します。

参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して、別のアドインまたは Outlook が保持するアクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。

次のコード例の CreateExceptionExample では、定期的な予定の件名を変更します。この予定は、トピック「[定期的な一連の予定から特定の予定を検索する](how-to-find-a-specific-appointment-in-a-recurring-appointment-series.md)」で作成したものです。その後、結果の Exception オブジェクトの AppointmentItem プロパティを使用して、予定の例外に対応する AppointmentItem を取得します。 さらに、CreateExceptionExample では、予定の例外の開始時刻と終了時刻を変更します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateExceptionExample()
{
    Outlook.AppointmentItem appt = Application.Session.
        GetDefaultFolder(Outlook.OlDefaultFolders.olFolderCalendar).
        Items.Find(
        "[Subject]='Recurring Appointment DaysOfWeekMask Example'")
        as Outlook.AppointmentItem;
    if (appt != null)
    {
        try
        {
            Outlook.RecurrencePattern pattern =
                appt.GetRecurrencePattern();
            Outlook.AppointmentItem myInstance =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (myInstance != null)
            {
                myInstance.Subject = "My Exception";
                myInstance.Save();
                Outlook.RecurrencePattern newPattern =
                    appt.GetRecurrencePattern();
                Outlook.Exception myException =
                    newPattern.Exceptions[1];
                if (myException != null)
                {
                    Outlook.AppointmentItem myNewInstance =
                        myException.AppointmentItem;
                    myNewInstance.Start =
                        DateTime.Parse("7/21/2006 1:00 PM");
                    myNewInstance.End =
                        DateTime.Parse("7/21/2006 2:00 PM");
                    myNewInstance.Save();
                }
            }
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

