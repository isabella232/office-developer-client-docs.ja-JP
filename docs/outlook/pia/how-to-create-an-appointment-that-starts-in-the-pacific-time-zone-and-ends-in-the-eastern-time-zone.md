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
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="aabfe-102">太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する</span><span class="sxs-lookup"><span data-stu-id="aabfe-102">Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone</span></span>

<span data-ttu-id="aabfe-p101">予定の期間内に、ユーザーが予定の開始時とは異なるタイム ゾーンに移動する場合があります。この例では、太平洋タイム ゾーン (UTC-8) で開始して東部タイム ゾーン (UTC-5) で終了する予定を作成します。</span><span class="sxs-lookup"><span data-stu-id="aabfe-p101">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts. This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="aabfe-105">例</span><span class="sxs-lookup"><span data-stu-id="aabfe-105">Example</span></span>

<span data-ttu-id="aabfe-106">このコードサンプルでは[](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) 、Microsoft Windows で認識されるすべてのタイムゾーンを表すタイムゾーンオブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="aabfe-106">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows.</span></span> <span data-ttu-id="aabfe-107">また、 [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\))オブジェクトを使用して、 [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\))オブジェクトの[starttimezone](https://msdn.microsoft.com/library/bb623657\(v=office.15\))プロパティと[endtimezone](https://msdn.microsoft.com/library/bb612198\(v=office.15\))プロパティを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="aabfe-107">It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="aabfe-108">Outlook では、すべての日付が現地時刻で表示されます。これは、ユーザーの現在のタイムゾーンで表示され、Windows のコントロールパネルでユーザーの設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="aabfe-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="aabfe-109">Outlook では、[開始日](https://msdn.microsoft.com/library/bb647263\(v=office.15\))、[終了](https://msdn.microsoft.com/library/bb623715\(v=office.15\))日などのプロパティを現地時刻で設定または取得することもできます。</span><span class="sxs-lookup"><span data-stu-id="aabfe-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="aabfe-110">ただし、Outlook では、日付と時刻の値は、現地時刻ではなく協定世界時 (UTC) として保存されます。</span><span class="sxs-lookup"><span data-stu-id="aabfe-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="aabfe-111">予定の内部値を調べると、 [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\))オブジェクトを使用して、内部の日付と時刻の値が、対応する UTC の日付と時刻の値に変換されたローカルの日付と時刻の値と等しいことがわかります。</span><span class="sxs-lookup"><span data-stu-id="aabfe-111">If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="aabfe-112">Outlook は、タイム ゾーンの情報を使用して、予定を保存するときは予定を正しい UTC 時刻にマップし、予定表にアイテムを表示するときは正しい現地時刻に戻します。</span><span class="sxs-lookup"><span data-stu-id="aabfe-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="aabfe-113">starttimezone を変更すると、常にローカルタイムゾーンで表され、タイムゾーンによって返されるオブジェクトの[currenttimezone](https://msdn.microsoft.com/library/bb612024\(v=office.15\))プロパティで表されます[](https://msdn.microsoft.com/library/bb645170\(v=office.15\))。</span><span class="sxs-lookup"><span data-stu-id="aabfe-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) property of the object returned by [TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)).</span></span> <span data-ttu-id="aabfe-114">同様に、EndTimeZone を変更すると、Application.TimeZones によって返されるオブジェクトの CurrentTimeZone プロパティで表される、常に現地のタイム ゾーンで表現される Appointment.End の値に影響があります。</span><span class="sxs-lookup"><span data-stu-id="aabfe-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="aabfe-115">TimeZones オブジェクトから特定の TimeZone を取得するには、Windows レジストリに含まれる TimeZone に対する現地に依存しないキーを使用します。</span><span class="sxs-lookup"><span data-stu-id="aabfe-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="aabfe-116">ロケールに依存`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`しない TimeZone キーは、次のキーの下に表示されます。</span><span class="sxs-lookup"><span data-stu-id="aabfe-116">Locale-independent TimeZone keys are listed under the following key: `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`.</span></span>

<span data-ttu-id="aabfe-117">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="aabfe-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="aabfe-118">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aabfe-118">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="aabfe-119">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aabfe-119">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="aabfe-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="aabfe-120">See also</span></span>

- [<span data-ttu-id="aabfe-121">予定</span><span class="sxs-lookup"><span data-stu-id="aabfe-121">Appointments</span></span>](appointments.md)

