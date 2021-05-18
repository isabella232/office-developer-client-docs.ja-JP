---
title: 定期的な一連の予定から特定の予定を検索する
TOCTitle: Find a specific appointment in a recurring appointment series
ms:assetid: 01f55f04-7245-4325-a354-50a6eb270a31
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184586(v=office.15)
ms:contentKeyID: 55119812
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 19502895996d4777f2d1a6887aa80883a5398a09
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320253"
---
# <a name="find-a-specific-appointment-in-a-recurring-appointment-series"></a>定期的な一連の予定から特定の予定を検索する

この例では、一連の定期的な予定のうちの特定の予定を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを取得する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

特定の日付および時刻に発生する定期的な予定のインスタンスを見つけるには、[RecurrencePattern](https://msdn.microsoft.com/library/bb622806\(v=office.15\)) オブジェクトの [GetOccurrence(DateTime)](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) メソッドを使用して、 **AppointmentItem** オブジェクトを取得します。

定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。 この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。 Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。 C\# では、そのオブジェクトのメモリを明示的に解放します。

参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。

次のコード例の CheckOccurrenceExample では、「[週単位パターンの定期的な予定を作成する](how-to-create-a-recurring-appointment-that-has-a-weekly-pattern.md)」で作成した定期的な予定を使用します。 GetOccurrence メソッドを呼び出して、定期的な予定の開始日と時刻が指定されているかどうかを調べます。 定期的な予定のインスタンスの開始日と時刻が指定の情報と一致しない場合でもプロシージャが続行されるように、この例では try…catch ブロックを使用しています。 CheckOccurrenceExample では、一連の定期的な予定に含まれる予定ごとに GetOccurrence メソッドを呼び出してから、singleAppt 変数をテストして、その変数が null 参照に設定されているかどうかを調べます。この null 参照は、メソッドが失敗して **AppointmentItem** オブジェクトが返されなかったことを示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CheckOccurrenceExample()
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
            Outlook.AppointmentItem singleAppt =
                pattern.GetOccurrence(DateTime.Parse(
                "7/21/2006 2:00 PM"))
                as Outlook.AppointmentItem;
            if (singleAppt != null)
            {
                Debug.WriteLine("7/21/2006 2:00 PM occurrence found.");
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

