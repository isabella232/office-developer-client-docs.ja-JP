---
title: 予定アイテムのリマインダーを作成する
TOCTitle: Create a reminder for an appointment item
ms:assetid: 85e772f0-65ac-4abc-8286-9099882a2400
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184623(v=office.15)
ms:contentKeyID: 55119814
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 164e744e03ab0984265736673c71d2d0bf57bf45
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405974"
---
# <a name="create-a-reminder-for-an-appointment-item"></a>予定アイテムのリマインダーを作成する

この例では、[ReminderSet](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) プロパティを使用して予定アイテムのリマインダーを作成する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


Outlook では、[AppointmentItem](https://msdn.microsoft.com/library/bb624262\(v=office.15\)) オブジェクトの [ReminderSet](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) プロパティを使用して、予定に事前通知を設定できます。このプロパティは、予定に対して事前通知が作成されているかどうかを示します。 ReminderSet プロパティを true に設定すると通知が作成され、 false に設定すると通知が削除されます。

次のコード例の ReminderExample では、California 州の Napa で開催されるワイン試飲会のプライベートな予定に対するリマインダーを作成して、その予定の開始 2 時間前に通知されるようにリマインダーを設定します。 ReminderExample では、まず、Outlook **AppointmentItem** オブジェクトを作成します。 その後、アイテムの [Sensitivity](https://msdn.microsoft.com/library/bb623503\(v=office.15\)) プロパティを [olPrivate](https://msdn.microsoft.com/library/bb645125\(v=office.15\)) に設定します。 これにより、予定がプライベートな予定であることを示します。 その他の予定のプロパティ ([Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) と [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) の時刻など) を設定した後で、ReminderExample では [ReminderMinutesBeforeStart](https://msdn.microsoft.com/library/bb644528\(v=office.15\)) プロパティを設定して、予定の開始何分前にリマインダーが表示ようにするかを指示します。 この例では、ReminderMinutesBeforeStart が 120 分 (2 時間) に設定されています。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void ReminderExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Wine Tasting";
    appt.Location = "Napa CA";
    appt.Sensitivity = Outlook.OlSensitivity.olPrivate;
    appt.Start = DateTime.Parse("10/21/2006 10:00 AM");
    appt.End = DateTime.Parse("10/21/2006 3:00 PM");
    appt.ReminderSet = true;
    appt.ReminderMinutesBeforeStart = 120;
    appt.Save();
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

