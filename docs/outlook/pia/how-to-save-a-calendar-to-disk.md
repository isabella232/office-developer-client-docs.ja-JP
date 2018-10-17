---
title: 予定表をディスクに保存する
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2f9a71d2743896ca6257e30efc7260ed11086ca5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405645"
---
# <a name="save-a-calendar-to-disk"></a><span data-ttu-id="5a901-102">予定表をディスクに保存する</span><span class="sxs-lookup"><span data-stu-id="5a901-102">Save a calendar to disk</span></span>

<span data-ttu-id="5a901-103">この例では、予定表全体を iCalendar (.ics) ファイル形式でディスクに保存する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5a901-103">This example shows how to save an entire calendar to disk in the iCalendar (.ics) file format.</span></span>

## <a name="example"></a><span data-ttu-id="5a901-104">例</span><span class="sxs-lookup"><span data-stu-id="5a901-104">Example</span></span>

<span data-ttu-id="5a901-p101">このコード サンプルでは、予定表全体または予定表のある範囲の予定をディスクに保存する処理をサポートする [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) オブジェクトを使用します。Outlook では、定期的な予定が .ics ファイルに個別の予定として保存されないように, .ics ファイルが自動的に最適化されます。保存する予定表のサイズによっては、ディスクへの予定表の保存にはかなりの時間がかかる場合があります。予定表を保存している間、ユーザーは Outlook ウィンドウを操作できません。</span><span class="sxs-lookup"><span data-stu-id="5a901-p101">This code sample uses the [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) object that supports saving a whole calendar or a range of appointments from the calendar to disk. Outlook automatically optimizes an .ics file so that recurring appointments are not saved as individual appointments in the .ics file. Depending on the size of the calendar being saved, saving a calendar to disk can take a significant amount of time. While saving the calendar, the Outlook window appears unresponsive to the user.</span></span>

<span data-ttu-id="5a901-p102">コード サンプルでは、最初に、既定の予定表フォルダーで [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) を呼び出して、 **CalendarSharing** オブジェクトを取得します。次に、 **CalendarSharing** オブジェクトのプロパティを設定し、予定表全体を保存するかどうかや、"非公開" に指定されている予定の詳細を含めるかどうかといった、エクスポートの条件を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a901-p102">The code sample first calls [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) on the default Calendar folder to obtain a **CalendarSharing** object. Then it sets properties of the **CalendarSharing** object to specify criteria for the export, such as whether to save the entire calendar and include details of appointments that are marked "private".</span></span>

<span data-ttu-id="5a901-111">予定表の情報を .ics ファイル形式に保存するには、**CalendarSharing** オブジェクトの [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="5a901-111">To save the calendar information in .ics file format, the code sample calls the [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) method of the **CalendarSharing** object.</span></span>

<span data-ttu-id="5a901-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5a901-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="5a901-113">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5a901-113">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="5a901-114">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5a901-114">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SaveCalendarToDisk(ByVal calendarFileName As String)
    If String.IsNullOrEmpty(calendarFileName) Then
        Throw New ArgumentException( _
        "Parameter must contain a value.", "calendarFileName")
    End If

    Dim calendar As Outlook.Folder = TryCast( _
        Application.Session.GetDefaultFolder(_
        Outlook.OlDefaultFolders.olFolderCalendar), Outlook.Folder)
    Dim exporter As Outlook.CalendarSharing = _
        calendar.GetCalendarExporter()

    '' Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails
    exporter.IncludeAttachments = True
    exporter.IncludePrivateDetails = True
    exporter.RestrictToWorkingHours = False
    exporter.IncludeWholeCalendar = True

    '' Save the calendar to disk
    exporter.SaveAsICal(calendarFileName)
End Sub
```


```csharp
private void SaveCalendarToDisk(string calendarFileName)
{
    if (string.IsNullOrEmpty(calendarFileName))
        throw new ArgumentException("calendarFileName", 
        "Parameter must contain a value.");

    Outlook.Folder calendar = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderCalendar) as Outlook.Folder;
    Outlook.CalendarSharing exporter = calendar.GetCalendarExporter();

    // Set the properties for the export
    exporter.CalendarDetail = Outlook.OlCalendarDetail.olFullDetails;
    exporter.IncludeAttachments = true;
    exporter.IncludePrivateDetails = true;
    exporter.RestrictToWorkingHours = false;
    exporter.IncludeWholeCalendar = true;

    // Save the calendar to disk
    exporter.SaveAsICal(calendarFileName);
}
```

## <a name="see-also"></a><span data-ttu-id="5a901-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="5a901-115">See also</span></span>

- [<span data-ttu-id="5a901-116">予定表</span><span class="sxs-lookup"><span data-stu-id="5a901-116">Calendar</span></span>](calendar.md)
