---
title: 予定表をディスクに保存する
TOCTitle: Save a calendar to disk
ms:assetid: f1b57bd0-c972-4b86-8870-f26290f28050
ms:mtpsurl: https://msdn.microsoft.com/library/Bb647583(v=office.15)
ms:contentKeyID: 55119827
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b07df7458f80b751077358ac3c53ad41032d1080
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712506"
---
# <a name="save-a-calendar-to-disk"></a>予定表をディスクに保存する

この例では、予定表全体を iCalendar (.ics) ファイル形式でディスクに保存する方法を示します。

## <a name="example"></a>例

このコード サンプルでは、予定表全体または予定表のある範囲の予定をディスクに保存する処理をサポートする [CalendarSharing](https://msdn.microsoft.com/library/bb624344\(v=office.15\)) オブジェクトを使用します。Outlook では、定期的な予定が .ics ファイルに個別の予定として保存されないように, .ics ファイルが自動的に最適化されます。保存する予定表のサイズによっては、ディスクへの予定表の保存にはかなりの時間がかかる場合があります。予定表を保存している間、ユーザーは Outlook ウィンドウを操作できません。

コード サンプルでは、最初に、既定の予定表フォルダーで [GetCalendarExporter](https://msdn.microsoft.com/library/bb610021\(v=office.15\)) を呼び出して、 **CalendarSharing** オブジェクトを取得します。次に、 **CalendarSharing** オブジェクトのプロパティを設定し、予定表全体を保存するかどうかや、"非公開" に指定されている予定の詳細を含めるかどうかといった、エクスポートの条件を指定します。

予定表の情報を .ics ファイル形式に保存するには、**CalendarSharing** オブジェクトの [SaveAsICal](https://msdn.microsoft.com/library/bb644844\(v=office.15\)) メソッドを呼び出します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [予定表](calendar.md)

