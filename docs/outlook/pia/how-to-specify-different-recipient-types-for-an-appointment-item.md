---
title: 予定アイテムに異なる受信者の種類を指定する
TOCTitle: Specify different recipient types for an appointment item
ms:assetid: 83aedc8f-adc0-453d-8e71-1bb9aacc7993
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184622(v=office.15)
ms:contentKeyID: 55119807
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: beb29c46d590938d1650dac0c862dd5f898333fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335414"
---
# <a name="specify-different-recipient-types-for-an-appointment-item"></a>予定アイテムに異なる受信者の種類を指定する

この例では、[OlMeetingRecipientType](https://msdn.microsoft.com/library/bb623431\(v=office.15\)) 列挙値を使用して予定アイテムに異なる受信者の種類を指定する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

会議出席依頼を表す [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) オブジェクトに受信者を追加するには、 OlMeetingRecipientType 列挙値を使用して、メッセージの受信者が必須または任意の出席者か、それともリソース (部屋や機器など) かを指定します。

次のコード例の SetRecipientTypeForAppt では、**AppointmentItem** オブジェクトを作成し、そのオブジェクトにプロパティを設定して、必須および任意の出席者を追加します。 また、会議用の会議室も追加します。 [MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) プロパティを [olMeeting](https://msdn.microsoft.com/library/bb644590\(v=office.15\)) に設定し、予定が会議出席依頼であることを示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SetRecipientTypeForAppt()
{
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.Subject = "Customer Review";
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting;
    appt.Location = "36/2021";
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM");
    appt.End = DateTime.Parse("10/20/2006 11:00 AM");
    Outlook.Recipient recipRequired =
        appt.Recipients.Add("Ryan Gregg");
    recipRequired.Type =
        (int)Outlook.OlMeetingRecipientType.olRequired;
    Outlook.Recipient recipOptional =
        appt.Recipients.Add("Peter Allenspach");
    recipOptional.Type =
        (int)Outlook.OlMeetingRecipientType.olOptional;
    Outlook.Recipient recipConf =
        appt.Recipients.Add("Conf Room 36/2021 (14) AV");
    recipConf.Type =
        (int)Outlook.OlMeetingRecipientType.olResource;
    appt.Recipients.ResolveAll();
    appt.Display(false);
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

