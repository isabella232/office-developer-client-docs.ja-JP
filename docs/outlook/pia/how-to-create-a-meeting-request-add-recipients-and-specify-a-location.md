---
title: 会議出席依頼を作成し、受信者を追加して、場所を指定する
TOCTitle: Create a meeting request, add recipients, and specify a location
ms:assetid: 3053c27e-34d9-440e-9b66-06de940c2813
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644964(v=office.15)
ms:contentKeyID: 55119873
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: high
ms.openlocfilehash: 410a90388ec9b3237eb150f74c08818b8b08739e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590794"
---
# <a name="create-a-meeting-request-add-recipients-and-specify-a-location"></a>会議出席依頼を作成し、受信者を追加して、場所を指定する

この例では、受信者と会議の時刻および場所を指定する会議出席依頼として予定アイテムを作成し、その予定をインスペクターに表示します。

## <a name="example"></a>例

Outlook の場合、会議出席依頼は [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) です。 予定アイテムを会議出席依頼として設定するには、[MeetingStatus](https://msdn.microsoft.com/library/bb611417\(v=office.15\)) プロパティを **olMeeting** に設定する必要があります。 [Recipient](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) オブジェクトの [Type](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) プロパティを使用して、会議出席者がオプションかどうかや、受信者が実際には出席者ではなく会議のリソースであるかどうかを指定します。

Visual Studio を使用してこのコード サンプルをテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートする際に、最初に必ず Microsoft Outlook 15.0 Object Library コンポーネントへの参照を追加し、そして Outlook 変数を指定します。**Imports** または **using** ステートメントは、コード サンプル中の関数の前に直接置かれず、Public クラス宣言の前に追加する必要があります。次のプログラムは、Visual Basic および C\#でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SetRecipientTypeForAppt()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    appt.Subject = "Customer Review"
    appt.MeetingStatus = Outlook.OlMeetingStatus.olMeeting
    appt.Location = "36/2021"
    appt.Start = DateTime.Parse("10/20/2006 10:00 AM")
    appt.End = DateTime.Parse("10/20/2006 11:00 AM")
    Dim recipRequired As Outlook.Recipient = _
        appt.Recipients.Add("Ryan Gregg")
    recipRequired.Type = _
        Outlook.OlMeetingRecipientType.olRequired
    Dim recipOptional As Outlook.Recipient = _
        appt.Recipients.Add("Peter Allenspach")
    recipOptional.Type = _
        Outlook.OlMeetingRecipientType.olOptional
    Dim recipConf As Outlook.Recipient = _
        appt.Recipients.Add("Conf Room 36/2021 (14) AV")
    recipConf.Type = _
        Outlook.OlMeetingRecipientType.olResource
    appt.Recipients.ResolveAll()
    appt.Display(False)
End Sub
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

- [会議出席依頼](meeting-requests.md)

