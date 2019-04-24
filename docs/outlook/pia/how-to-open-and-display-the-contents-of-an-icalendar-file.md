---
title: iCalendar ファイルを開いて内容を表示する
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fad55b4e9b98a2157d1efdab83d5495cd2169429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320021"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a>iCalendar ファイルを開いて内容を表示する

この例では、ファイル内の予定が単一の予定または定期的な予定か、それとも複数の予定かに応じて、iCalendar ファイルのコンテンツを開いて表示する方法を示します。

## <a name="example"></a>例

このコード例では、まず [NameSpace](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) オブジェクトの [OpenSharedItem](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドを使用して、iCalendar ファイルを単一の予定の iCalendar ファイルとして開くことを試みます。それに成功した場合は、予定アイテムの詳細をインスペクター ウィンドウに表示します。ただし、そのアイテムを既定のストアにコピーすることはしません。ファイルを単一の予定の iCalendar ファイルとして開くことができない場合は、 [NameSpace](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) オブジェクトの **OpenSharedFolder** メソッドを使用して、そのコンテンツを既定のストアの新しい予定表としてインポートすることを試みます。インポートに成功した場合は、予定表をエクスプローラー ウィンドウに表示します。

このコード サンプルは、[「ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする」](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)で定義されている OutlookItem ヘルパー クラスを使用して、予定アイテムを表示する **OutlookItem.Display** メソッドを簡単に呼び出します。最初にアイテムをキャストする必要はありません。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub OpenICalendarFile(ByVal fileName As String)
    If String.IsNullOrEmpty(fileName) Then
        Throw New ArgumentException(_
        "Parameter must contain a value.", "exportFileName")
    End If
    If Not File.Exists(fileName) Then
        Throw New FileNotFoundException(fileName)
    End If

    '' First try to open the icalendar file as an appointment 
    '' (not a calendar folder).
    Dim item As Object = Nothing
    Try
         item = Application.Session.OpenSharedItem(fileName)
    Catch
    End Try

    If Not item Is Nothing Then
        '' Display the item
        Dim olItem As OutlookItem = New OutlookItem(item)
        olItem.Display()
        Return
    End If

    '' If unsucessful in opening it as an item, 
    '' try opening it as a folder
    Dim importedFolder As Outlook.Folder = Nothing
    Try
        importedFolder = TryCast( _
            Application.Session.OpenSharedFolder(fileName), _
            Outlook.Folder)
    Catch
    End Try

    '' If sucessful, open the folder in a new explorer window
    If Not importedFolder Is Nothing Then
        Dim explorer As Outlook.Explorer = _
            Application.Explorers.Add( _
            importedFolder, _
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal)
        explorer.Display()
    End If
End Sub
```


```csharp
private void OpenICalendarFile(string fileName)
{
    if (string.IsNullOrEmpty(fileName))
        throw new ArgumentException("exportFileName", 
        "Parameter must contain a value.");
    if (!File.Exists(fileName))
        throw new FileNotFoundException(fileName);

    // First try to open the icalendar file as an appointment 
    // (not a calendar folder).
    object item = null;
    try
    {
        item = Application.Session.OpenSharedItem(fileName);
    }
    catch
    { }

    if (item != null)
    {
         // Display the item
         OutlookItem olItem = new OutlookItem(item);
         olItem.Display();
         return;
    }

    // If unsucessful in opening it as an item, 
    // try opening it as a folder
    Outlook.Folder importedFolder = null;
    try
    {
        importedFolder = Application.Session.OpenSharedFolder(
            fileName, Type.Missing, Type.Missing, Type.Missing) 
            as Outlook.Folder;
    }
    catch
    { }

    // If sucessful, open the folder in a new explorer window
    if (importedFolder != null)
    {
        Outlook.Explorer explorer =
            Application.Explorers.Add(importedFolder, 
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        explorer.Display();
    }
}
```

## <a name="see-also"></a>関連項目

- [予定表](calendar.md)

