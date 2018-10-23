---
title: 予定表で指定した期間内の空き時間スケジュールを共有する
TOCTitle: Share Free/Busy schedule within a specified period in a calendar
ms:assetid: 1d038f56-80dd-42fd-809b-f5b3a47cd5ee
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609503(v=office.15)
ms:contentKeyID: 55119824
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 359b328002b711930eab6c029474b3b39cbc184e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406191"
---
# <a name="share-freebusy-schedule-within-a-specified-period-in-a-calendar"></a><span data-ttu-id="628a2-102">予定表で指定した期間内の空き時間スケジュールを共有する</span><span class="sxs-lookup"><span data-stu-id="628a2-102">Share Free/Busy schedule within a specified period in a calendar</span></span>

<span data-ttu-id="628a2-103">この例では、予定表の指定した週の空き時間スケジュールを取得し、ユーザーに対して予定の有無と件名を表示します。</span><span class="sxs-lookup"><span data-stu-id="628a2-103">This example obtains the free/busy schedule within a specified week from a calendar and displays the free, busy, and subject details to the user.</span></span>

## <a name="example"></a><span data-ttu-id="628a2-104">例</span><span class="sxs-lookup"><span data-stu-id="628a2-104">Example</span></span>

<span data-ttu-id="628a2-p101">このコード例では、[Folder](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) オブジェクトの [GetCalendarExporter](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) メソッドを使用して既定の予定表フォルダーの [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) オブジェクトを、指定された特定の週にわたって取得します。その後、 [CalendarSharing](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) オブジェクトの **ForwardAsICal** メソッドを呼び出し、iCalendar ペイロードを含むメッセージを表示します。</span><span class="sxs-lookup"><span data-stu-id="628a2-p101">This code sample uses the [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) method of the [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object to obtain a [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object for the default Calendar folder for a specific one-week period. It then calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method on the **CalendarSharing** object and displays the message with an iCalendar payload.</span></span>

<span data-ttu-id="628a2-107">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="628a2-107">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="628a2-108">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="628a2-108">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="628a2-109">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="628a2-109">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub DemoCalendarSharing()
    ' Get instance of CalendarSharing object
    Dim calShare As Outlook.CalendarSharing = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar). _
        GetCalendarExporter()
    ' Free busy and subject details
    calShare.CalendarDetail = _
        Outlook.OlCalendarDetail.olFreeBusyAndSubject
    ' Set start and end dates
    calShare.StartDate = DateTime.Today
    calShare.EndDate = calShare.StartDate.AddDays(1)
    ' Call ForwardAsICal method
    Dim mail As Outlook.MailItem = _
        calShare.ForwardAsICal( _
        Outlook.OlCalendarMailFormat.olCalendarMailFormatDailySchedule)
    ' Add recipient
    mail.Recipients.Add("someone@example.com")
    mail.Recipients.ResolveAll()
    ' Set subject
    Dim CalName As String = _
    Application.Session.GetDefaultFolder( _
    Outlook.OlDefaultFolders.olFolderCalendar).Name
    mail.Subject = _
        Application.Session.CurrentUser.Name & _
        CalName.PadLeft(CalName.Length + 1)
    ' Display calendar sharing item
    mail.Display(False)
End Sub
```

```csharp
private void DemoCalendarSharing()
{
    // Get instance of CalendarSharing object
    Outlook.CalendarSharing calShare =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderCalendar).
        GetCalendarExporter();
    // Free busy and subject details
    calShare.CalendarDetail =
        Outlook.OlCalendarDetail.olFreeBusyAndSubject;
    // Set start and end dates
    calShare.StartDate = DateTime.Today;
    calShare.EndDate = calShare.StartDate.AddDays(1);
    // Call ForwardAsICal method
    Outlook.MailItem mail =
        calShare.ForwardAsICal(Outlook.OlCalendarMailFormat
        .olCalendarMailFormatDailySchedule);
    // Add recipient
    mail.Recipients.Add("someone@example.com");
    mail.Recipients.ResolveAll();
    // Set subject
    string CalName =
        Application.Session.GetDefaultFolder
    (Outlook.OlDefaultFolders.olFolderCalendar).Name;
    mail.Subject =
        Application.Session.CurrentUser.Name +
        CalName.PadLeft(CalName.Length + 1);
    // Display calendar sharing item
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="628a2-110">関連項目</span><span class="sxs-lookup"><span data-stu-id="628a2-110">See also</span></span>

- [<span data-ttu-id="628a2-111">予定表</span><span class="sxs-lookup"><span data-stu-id="628a2-111">Calendar</span></span>](calendar.md)
