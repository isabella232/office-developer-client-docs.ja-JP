---
title: 太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する
TOCTitle: Create an appointment that starts in the Pacific Time Zone and ends in the Eastern Time Zone
ms:assetid: ba19532b-df31-4384-8816-e64e6eecbe53
ms:mtpsurl: https://msdn.microsoft.com/library/Bb623388(v=office.15)
ms:contentKeyID: 55119808
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 9cb21bddb425adb54082dbe21b32653e1fe3ca75
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406079"
---
# <a name="create-an-appointment-that-starts-in-the-pacific-time-zone-and-ends-in-the-eastern-time-zone"></a><span data-ttu-id="770ce-102">太平洋タイム ゾーンで開始して東部タイム ゾーンで終了する予定を作成する</span><span class="sxs-lookup"><span data-stu-id="770ce-102">How to: Create an Appointment that Starts in the Pacific Time Zone and Ends in the Eastern Time Zone</span></span>

<span data-ttu-id="770ce-p101">予定の期間内に、ユーザーが予定の開始時とは異なるタイム ゾーンに移動する場合があります。この例では、太平洋タイム ゾーン (UTC-8) で開始して東部タイム ゾーン (UTC-5) で終了する予定を作成します。</span><span class="sxs-lookup"><span data-stu-id="770ce-p101">Occasionally, an appointment may span over a period of time during which the user may have traveled to a different time zone than when the appointment starts. This example creates an appointment that begins in the Pacific Time Zone (UTC-8) and ends in the Eastern Time Zone (UTC-5).</span></span>

## <a name="example"></a><span data-ttu-id="770ce-105">例</span><span class="sxs-lookup"><span data-stu-id="770ce-105">Example</span></span>

<span data-ttu-id="770ce-p102">このコード サンプルでは、Microsoft Windows で認識されるすべてのタイム ゾーンを表す [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) オブジェクトを使用します。また、 [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) オブジェクトを使用して [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) プロパティを設定または取得し、 [AppointmentItem](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) オブジェクトの [EndTimeZone](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="770ce-p102">This code sample uses the [TimeZones](https://msdn.microsoft.com/library/bb611081\(v=office.15\)) object that represents all the time zones recognized in Microsoft Windows. It also uses the [TimeZone](https://msdn.microsoft.com/library/bb646259\(v=office.15\)) object to set or get the [StartTimeZone](https://msdn.microsoft.com/library/bb623657\(v=office.15\)) property and the [EndTimeZone](https://msdn.microsoft.com/library/bb612198\(v=office.15\)) property on the [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) object.</span></span>

<span data-ttu-id="770ce-108">Outlook では、すべての日付がローカル時刻で表示されます。この時刻は、ユーザーの現在のタイム ゾーンで表現され、Windows の [コントロール パネル] のユーザー設定によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="770ce-108">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel.</span></span> <span data-ttu-id="770ce-109">また、Outlook では、[Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) や [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)) などのプロパティがローカル時刻で設定または取得されます。</span><span class="sxs-lookup"><span data-stu-id="770ce-109">Outlook also sets or gets properties, such as [Start](https://msdn.microsoft.com/library/bb647263\(v=office.15\)) and [End](https://msdn.microsoft.com/library/bb623715\(v=office.15\)), in local time.</span></span> <span data-ttu-id="770ce-110">ただし、Outlook では、日付値と時刻値をローカル時刻ではなく協定世界時 (UTC) として保存します。</span><span class="sxs-lookup"><span data-stu-id="770ce-110">However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time.</span></span> <span data-ttu-id="770ce-111">[PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを使用して Appointment.Start の内部値を調べると、日付と時刻の内部値は、ローカルの日付と時刻の値を同等の UTC の日付と時刻の値に変換したものと同じになることがわかります。</span><span class="sxs-lookup"><span data-stu-id="770ce-111">Outlook displays all dates in local time, which is expressed in the user's current time zone, controlled by the user's settings in the Windows Control Panel. Outlook also sets or gets properties, such as Start and End , in local time. However, Outlook stores date and time values as Coordinated Universal Time (UTC) rather than local time. If you examine the internal value of Appointment.Start by using the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object, you would find the internal date and time value is equal to the local date and time value converted to the equivalent UTC date and time value.</span></span>

<span data-ttu-id="770ce-112">Outlook は、タイム ゾーンの情報を使用して、予定を保存するときは予定を正しい UTC 時刻にマップし、予定表にアイテムを表示するときは正しい現地時刻に戻します。</span><span class="sxs-lookup"><span data-stu-id="770ce-112">Outlook uses the time zone information to map the appointment to the correct UTC time when it saves an appointment, and into the correct local time when it displays the item in the calendar.</span></span> <span data-ttu-id="770ce-113">StartTimeZone の変更は、常にローカル タイム ゾーンで表現される Appointment.Start の値に影響します。このローカル タイム ゾーンは、[TimeZones](https://msdn.microsoft.com/library/bb645170\(v=office.15\)) によって返されるオブジェクトの [CurrentTimeZone](https://msdn.microsoft.com/library/bb612024\(v=office.15\)) で表されます。</span><span class="sxs-lookup"><span data-stu-id="770ce-113">Changing StartTimeZone affects the value of Appointment.Start, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by TimeZones .</span></span> <span data-ttu-id="770ce-114">同様に、 EndTimeZone を変更すると、 Application.TimeZones によって返されるオブジェクトの CurrentTimeZone プロパティで表される、常に現地のタイム ゾーンで表現される Appointment.End の値に影響があります。</span><span class="sxs-lookup"><span data-stu-id="770ce-114">Similarly, changing EndTimeZone affects the value of Appointment.End, which is always expressed in the local time zone, represented by the CurrentTimeZone property of the object returned by Application.TimeZones.</span></span>

<span data-ttu-id="770ce-115">TimeZones オブジェクトから特定の TimeZone を取得するには、Windows レジストリの TimeZone にロケールに依存しないキーを使用します。</span><span class="sxs-lookup"><span data-stu-id="770ce-115">You can retrieve a specific TimeZone from the TimeZones object by using the locale-independent key for the TimeZone in the Windows registry.</span></span> <span data-ttu-id="770ce-116">ロケールに依存しない TimeZone キーは、次のキーの下に一覧表示されます。`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones`</span><span class="sxs-lookup"><span data-stu-id="770ce-116">Locale-independent `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones` keys are listed under the following key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion\TimeZones.</span></span>

<span data-ttu-id="770ce-117">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="770ce-117">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="770ce-118">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="770ce-118">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="770ce-119">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="770ce-119">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>


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

## <a name="see-also"></a><span data-ttu-id="770ce-120">関連項目</span><span class="sxs-lookup"><span data-stu-id="770ce-120">See also</span></span>

- [<span data-ttu-id="770ce-121">予定</span><span class="sxs-lookup"><span data-stu-id="770ce-121">Appointments</span></span>](appointments.md)

