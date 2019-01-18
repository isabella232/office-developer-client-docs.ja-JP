---
title: 既定の定期的なパターンを使用して、定期的な予定を作成する
TOCTitle: Create a recurring appointment by using the default recurrence pattern
ms:assetid: 157bf1ae-2efe-4783-99ea-606722dde204
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184589(v=office.15)
ms:contentKeyID: 55119809
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: de58523e663349c43cc358f5b76896987a0f23b3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722817"
---
# <a name="create-a-recurring-appointment-by-using-the-default-recurrence-pattern"></a>既定の定期的なパターンを使用して、定期的な予定を作成する

この例では、既定の定期的なパターンを使用して定期的な予定を作成する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


Outlook で予定を作成するときには、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトを作成します。 予定は、AppointmentItem の [IsRecurring](https://msdn.microsoft.com/library/bb609491\(v=office.15\)) プロパティを true に設定することで定期的な予定になります。 IsRecurring は、直接設定することができません。 

ただし、[RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) オブジェクトを使用することで、定期的な予定を作成できます。 プログラムで定期的な予定を作成するには、**AppointmentItem** オブジェクトを作成し、**AppointmentItem** オブジェクトの [GetRecurrencePattern()](https://msdn.microsoft.com/library/bb652582\(v=office.15\)) メソッドを呼び出してから、**AppointmentItem** オブジェクトを保存します。 これにより、既定の定期的なパターンを使用する予定が作成されます。このパターンでは、予約は毎週予定が作成された曜日に発生し、終了日はありません。 RecurrencePattern オブジェクトを使用すると、指定した間隔 (日次、週次、月次、年次) で繰り返される定期的な予定を作成できます。 RecurrencePattern に間隔を指定しない場合、Outlook では既定の定期的なパターンが使用されます。

定期的な予定アイテムの作業を行うときは、以前の参照を解放し、定期的な予定アイテムへの新しい参照を取得してからアイテムにアクセスしたりアイテムを変更したりした後、作業が終了して変更を保存したら直ちに参照を解放する必要があります。 この方法は、定期的な **AppointmentItem** オブジェクトと、あらゆる [Exception](https://msdn.microsoft.com/library/bb610440\(v=office.15\)) オブジェクトまたは [RecurrencePattern](https://msdn.microsoft.com/library/bb608903\(v=office.15\)) に適用するものです。 Visual Basic で参照を解放するには、その既存のオブジェクトを Nothing に設定します。 C\# では、そのオブジェクトのメモリを明示的に解放します。

参照を解放してから新しい参照を取得しようとしても、前記のいずれかのオブジェクトに対して (別のアドインまたは Outlook で保持されている) アクティブな参照がまだある場合、新しい参照はオブジェクトの古いコピーをまだ指していることに注意してください。したがって、定期的な予定の作業が終了したら速やかに参照を解放することが重要です。

次の例の CreateRecurringAppointment では、**AppointmentItem** オブジェクトを作成します。 その後で、GetRecurrencePattern を呼び出します。 GetRecurrencePattern から RecurrencePattern オブジェクトが返され、AppointmentItem オブジェクトが保存されます。 これにより、既定の定期的なパターンを使用する定期的な予定が作成されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void CreateRecurringAppointment()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Weekly Extensibility Team Meeting";
    Outlook.RecurrencePattern pattern = appt.GetRecurrencePattern();
    appt.Save();
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

