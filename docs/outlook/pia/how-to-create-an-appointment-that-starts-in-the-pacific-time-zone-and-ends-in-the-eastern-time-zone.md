---
title: 太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e9a1b9d5f65d8683c08821d4cf0851f599f32030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349456"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a>太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する

予定の期間内に、ユーザーが予定の開始時とは異なるタイム ゾーンに移動する場合があります。この例では、太平洋タイム ゾーン (UTC-8) で開始して東部タイム ゾーン (UTC-5) で終了する予定を作成します。

## <a name="example"></a>例

このコード サンプルでは、Microsoft サービス で認識されるタイム ゾーンを表す[TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\))オブジェクトをWindows。 また [、TimeZone オブジェクトを使用](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) して、AppointmentItem オブジェクトの [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) プロパティと [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) プロパティを設定または [取得](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) します。

Outlookは、ユーザーの現在のタイム ゾーンで表され、ユーザーのコントロール パネルのユーザーの設定によって制御される、現地時間Windows表示されます。 Outlook、ローカル時間に Start や[End](https://msdn.microsoft.com/library/bb623715\(v=office.15\))などのプロパティを設定または取得します。 [](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) ただし、Outlook時刻の値は、現地時間ではなく協定世界時 (UTC) として格納されます。 [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))オブジェクトを使用して Appointment.Start の内部値を調べると、内部の日付と時刻の値が、同等の UTC 日付と時刻の値に変換されたローカルの日付と時刻の値と等しくなります。

Outlook は、タイム ゾーンの情報を使用して、予定を保存するときは予定を正しい UTC 時刻にマップし、予定表にアイテムを表示するときは正しい現地時刻に戻します。 StartTimeZone の変更は、TimeZones によって返されるオブジェクトの [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) プロパティによって表される、常にローカル タイム ゾーンで表される Appointment.Start の値に [影響](https://msdn.microsoft.com/library/bb645170\(v=office.15\))します。 同様に、EndTimeZone を変更すると、Application.TimeZones によって返されるオブジェクトの CurrentTimeZone プロパティで表される、常に現地のタイム ゾーンで表現される Appointment.End の値に影響があります。

TimeZones オブジェクトから特定の TimeZone を取得するには、Windows レジストリに含まれる TimeZone に対する現地に依存しないキーを使用します。 ロケールに依存しない TimeZone キーは、次のキーの下に一覧表示されます `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones` 。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```



```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```



```vb
Private Sub TimeZoneExample()
    Dim appt As Outlook.AppointmentItem = _
        CType(Application.CreateItem( _
        Outlook.OlItemType.olAppointmentItem), Outlook.AppointmentItem)
    Dim tzs As Outlook.TimeZones = Application.TimeZones
    ' Obtain timezone using indexer and locale-independent key
    Dim tzEastern As Outlook.TimeZone = tzs("Eastern Standard Time")
    Dim tzPacific As Outlook.TimeZone = tzs("Pacific Standard Time")
    appt.Subject = "SEA - JFK Flight"
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM")
    appt.StartTimeZone = tzPacific
    appt.End = DateTime.Parse("8/9/2006 5:30 PM")
    appt.EndTimeZone = tzEastern
    appt.Display(False)
End Sub
```



```csharp
private void TimeZoneExample()
{
    Outlook.AppointmentItem appt = Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    Outlook.TimeZones tzs = Application.TimeZones;
    // Obtain timezone using indexer and locale-independent key
    Outlook.TimeZone tzEastern = tzs["Eastern Standard Time"];
    Outlook.TimeZone tzPacific = tzs["Pacific Standard Time"];
    appt.Subject = "SEA - JFK Flight";
    appt.Start = DateTime.Parse("8/9/2006 8:00 AM");
    appt.StartTimeZone = tzPacific;
    appt.End = DateTime.Parse("8/9/2006 5:30 PM");
    appt.EndTimeZone = tzEastern; 
    appt.Display(false);
}
```

## <a name="see-also"></a>関連項目

- [予定](appointments.md)

