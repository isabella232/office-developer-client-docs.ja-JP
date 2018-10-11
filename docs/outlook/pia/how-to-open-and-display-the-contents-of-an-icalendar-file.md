---
title: iCalendar ファイルを開いて内容を表示する
TOCTitle: Open and display the contents of an iCalendar file
ms:assetid: 2066e404-7aaf-4fd2-bf5c-9604e3fc2681
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644609(v=office.15)
ms:contentKeyID: 55119818
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: dcebc65c651804148969c6260ecac72060bf9ef0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406779"
---
# <a name="open-and-display-the-contents-of-an-icalendar-file"></a><span data-ttu-id="0f20f-102">iCalendar ファイルを開いて内容を表示する</span><span class="sxs-lookup"><span data-stu-id="0f20f-102">Open and display the contents of an iCalendar file</span></span>

<span data-ttu-id="0f20f-103">この例では、ファイル内の予定が単一の予定または定期的な予定か、それとも複数の予定かに応じて、iCalendar ファイルのコンテンツを開いて表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0f20f-103">This example shows how to open and display the contents of an iCalendar file, depending on whether the file contains a single or recurrent appointment, or the file contains a group of appointments.</span></span>

## <a name="example"></a><span data-ttu-id="0f20f-104">例</span><span class="sxs-lookup"><span data-stu-id="0f20f-104">Example</span></span>

<span data-ttu-id="0f20f-p101">このコード例では、まず [NameSpace](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) オブジェクトの [OpenSharedItem](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドを使用して、iCalendar ファイルを単一の予定の iCalendar ファイルとして開くことを試みます。それに成功した場合は、予定アイテムの詳細をインスペクター ウィンドウに表示します。ただし、そのアイテムを既定のストアにコピーすることはしません。ファイルを単一の予定の iCalendar ファイルとして開くことができない場合は、 [NameSpace](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) オブジェクトの **OpenSharedFolder** メソッドを使用して、そのコンテンツを既定のストアの新しい予定表としてインポートすることを試みます。インポートに成功した場合は、予定表をエクスプローラー ウィンドウに表示します。</span><span class="sxs-lookup"><span data-stu-id="0f20f-p101">This code sample first tries to use the [OpenSharedItem](https://msdn.microsoft.com/library/bb645399\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to open the iCalendar file as a single-appointment iCalendar file. If it succeeds, it will display the appointment item details in an inspector window. However, it will not copy the item to the default store. If the sample cannot open the file as a single-appointment iCalendar file, then it will use the [OpenSharedFolder](https://msdn.microsoft.com/library/bb610157\(v=office.15\)) method of the **NameSpace** object to attempt to import the contents as a new calendar in the default store. If it succeeds in importing, then it will display the calendar in an explorer window.</span></span>

<span data-ttu-id="0f20f-110">このコード サンプルは、[「ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする」](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)で定義されている OutlookItem ヘルパー クラスを使用して、予定アイテムを表示する **OutlookItem.Display** メソッドを簡単に呼び出します。最初にアイテムをキャストする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0f20f-110">This code sample makes use of the OutlookItem helper class, defined in How to: Create a Helper Class to Access Common Outlook Item Members, to conveniently call the OutlookItem.Display method to display the appointment item without having to first cast the item.</span></span>

<span data-ttu-id="0f20f-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0f20f-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0f20f-112">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f20f-112">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0f20f-113">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0f20f-113">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0f20f-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="0f20f-114">See also</span></span>

- [<span data-ttu-id="0f20f-115">予定表</span><span class="sxs-lookup"><span data-stu-id="0f20f-115">Calendar</span></span>](calendar.md)

