---
title: 終日イベントの予定を作成する
TOCTitle: Create an appointment that is an all-day event
ms:assetid: a0d3baeb-6ed5-41b6-bef5-d6c1bb56fee3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184629(v=office.15)
ms:contentKeyID: 55119806
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b5065395afe39247f8113bc5223b0e3e403a02fa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28710826"
---
# <a name="create-an-appointment-that-is-an-all-day-event"></a>終日イベントの予定を作成する

この例では、[AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) プロパティを使用して終日イベントである予定を作成する方法を説明します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

イベントは、24 時間以上継続するアクティビティである点が定期的な予定とは異なります。イベントの例としては、展示会、セミナー、休暇などがあります。イベントおよび例年のイベントは、ユーザーの予定表では時間のブロックを占めるアイテムとしては表示されません。代わりに、バナーとして表示されます。バナーは、予定表の日ビューまたは週ビューの最上部に表示されます。終日の予定の場合、既定では、そのユーザーの時間は他のユーザーに対しては "予定あり" として表示されますが、イベントまたは例年のイベントの場合はユーザーの時間は "空き" として表示されます。

終日イベントをプログラムで作成する場合は、[AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトの [AllDayEvent](https://msdn.microsoft.com/library/bb610279\(v=office.15\)) プロパティを true に設定します。 その後で、AppointmentItem の [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) プロパティと [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) プロパティを設定します。 AllDayEvent プロパティを true に設定し、 Start および End プロパティを設定しないと、イベントはその日に発生し、予定として扱われ、予定表には予定あり状態が表示されます。 将来の日付でイベントが発生するようにする場合は、Start プロパティと End プロパティを設定する必要があります。

> [!NOTE]
> 予定を終日イベントにするには、Start プロパティをイベント開始日の午前 12 時 00 分  (午前 0 時) に設定し、End プロパティをイベント終了日の翌日の午前 12 時 00 分 に設定する必要があります。 Start または End の時刻を午前 12 時 00 分以外の日時値に設定すると、その予定は終日イベントではなく、複数日のイベントになります。 
>
> たとえば、期間が 1 日だけのイベントの場合は、Start プロパティをイベント開始日の午前 12 時 00 分 に設定し、End プロパティを次の日の午前 12 時 00 分 に設定します。 End プロパティは、常に、開始日の翌日以降の午前 12 時 00 分 に設定してください。

次のコード例の AllDayEventExample では、2007 年 6 月 11 日に開始し、2007 年 6 月 15 日に終了する終日イベントを作成しています。End プロパティが 2007 年 6 月 16 日の 12:00 A.M. に設定されていることに注意してください。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AllDayEventExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Developer's Conference";
    appt.AllDayEvent = true;
    appt.Start = DateTime.Parse("6/11/2007 12:00 AM");
    appt.End = DateTime.Parse("6/16/2007 12:00 AM");
    appt.Display(false);
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

