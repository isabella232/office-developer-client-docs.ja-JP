---
title: 電子メールで予定表情報を共有する
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 574b8ec24b330276ebd47952d5353c4d170ee8db
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406443"
---
# <a name="share-calendar-information-through-email"></a><span data-ttu-id="d4e29-102">電子メールで予定表情報を共有する</span><span class="sxs-lookup"><span data-stu-id="d4e29-102">Share calendar information through email</span></span>

<span data-ttu-id="d4e29-103">この例では、iCalendar 形式の予定表の情報を電子メールで共有する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d4e29-103">This example shows how to share information from a calendar by e-mail in the iCalendar format.</span></span>

## <a name="example"></a><span data-ttu-id="d4e29-104">例</span><span class="sxs-lookup"><span data-stu-id="d4e29-104">Example</span></span>

<span data-ttu-id="d4e29-p101">iCalendar 形式を使用すると、アイテムを他の Outlook クライアントや Outlook 以外のクライアントにインターネットの標準のメール形式とプロトコルを使用して送信できます。このコード例では、予定表フォルダーの情報を iCalendar 形式でエクスポートする機能をサポートする [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) オブジェクトを使用しています。</span><span class="sxs-lookup"><span data-stu-id="d4e29-p101">The iCalendar format allows you to send items to other Outlook or non-Outlook clients via standard Internet mail formats and protocols. The code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports exporting information from a calendar folder to the iCalendar format.</span></span>

<span data-ttu-id="d4e29-p102">このコード例では、まず既定の予定表フォルダーで [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) を呼び出して、 **CalendarSharing** オブジェクトを取得します。次に、 **CalendarSharing** オブジェクトのプロパティを設定して、エクスポートの条件 (予定表情報の期間など)、添付ファイルを含めるかどうか、および "非公開" と設定された予定の詳細を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4e29-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as the date range of calendar information, whether to include attachments, and details of appointments that are marked "private."</span></span>

<span data-ttu-id="d4e29-109">予定表の情報を電子メールで送信するには、**CalendarSharing** オブジェクトの [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="d4e29-109">To send the calendar information by e-mail, the code sample calls the [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="d4e29-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d4e29-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="d4e29-111">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d4e29-111">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="d4e29-112">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="d4e29-112">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub SendNextWeekToAddress(ByVal sendToAddresses As String)
    If String.IsNullOrEmpty(sendToAddresses) Then
        Throw New ArgumentException( _
            "Parameter must contain a value.", "sendToAddress")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = False
    exporter.RestrictToWorkingHours = False
    exporter.StartDate = DateTime.Today.Date
    exporter.EndDate = DateTime.Today.Date.AddDays(7)

    '' Create a new mail item
    Dim calendarMail As Outlook.MailItem = exporter.ForwardAsICal _
        (Outlook.OlCalendarMailFormat. _
        olCalendarMailFormatDailySchedule)
    calendarMail.To = sendToAddresses
    calendarMail.Send()
    calendarMail.Display()
End Sub
```

```csharp
private void SendNextWeekToAddress(string sendToAddresses)
{
    if (string.IsNullOrEmpty(sendToAddresses))
        throw new ArgumentException(
        "sendToAddress","Parameter must contain a value.");
    Outlook.Folder calendar = 
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar)
        as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = false;
    exporter.RestrictToWorkingHours = false;
    exporter.StartDate = DateTime.Today.Date;
    exporter.EndDate = DateTime.Today.Date.AddDays(7);

    // Create a new mail item
    Outlook.MailItem calendarMail = 
        exporter.ForwardAsICal(Outlook.OlCalendarMailFormat.
        olCalendarMailFormatDailySchedule);
    calendarMail.To = sendToAddresses;
    ((Outlook.MailItemClass)calendarMail).Send();
    ((Outlook.MailItemClass)calendarMail).Display(Type.Missing);
}
```

## <a name="see-also"></a><span data-ttu-id="d4e29-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="d4e29-113">See also</span></span>

- [<span data-ttu-id="d4e29-114">予定表</span><span class="sxs-lookup"><span data-stu-id="d4e29-114">Calendar</span></span>](calendar.md)

