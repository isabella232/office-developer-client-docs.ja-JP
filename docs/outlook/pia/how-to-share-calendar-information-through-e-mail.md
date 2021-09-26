---
title: 電子メールで予定表情報を共有する
TOCTitle: Share calendar information through email
ms:assetid: 3382010c-0a16-4dca-a99e-669e9178354e
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609881(v=office.15)
ms:contentKeyID: 55119817
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: d6e1031e5d4b387aee7297dd91584f0916b4f00b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608943"
---
# <a name="share-calendar-information-through-email"></a>電子メールで予定表情報を共有する

この例では、iCalendar 形式の予定表の情報を電子メールで共有する方法を示します。

## <a name="example"></a>例

iCalendar 形式を使用すると、アイテムを他の Outlook クライアントや Outlook 以外のクライアントにインターネットの標準のメール形式とプロトコルを使用して送信できます。このコード例では、予定表フォルダーの情報を iCalendar 形式でエクスポートする機能をサポートする [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) オブジェクトを使用しています。

このコード例では、まず既定の予定表フォルダーで [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) を呼び出して、 **CalendarSharing** オブジェクトを取得します。次に、 **CalendarSharing** オブジェクトのプロパティを設定して、エクスポートの条件 (予定表情報の期間など)、添付ファイルを含めるかどうか、および "非公開" と設定された予定の詳細を指定します。

予定表の情報を電子メールで送信するには、**CalendarSharing** オブジェクトの [ForwardAsICal](https://msdn.microsoft.com/library/bb652866\(v=office.15\)) メソッドを呼び出します。

Visual Studio を使用してこのコード サンプルをテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートする際に、最初に必ず Microsoft Outlook 15.0 Object Library コンポーネントへの参照を追加し、そして Outlook 変数を指定します。**Imports** または **using** ステートメントは、コード サンプル中の関数の前に直接置かれず、Public クラス宣言の前に追加する必要があります。次のプログラムは、Visual Basic および C\#でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [予定表](calendar.md)

