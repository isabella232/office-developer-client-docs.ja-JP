---
title: フォルダーを選択してフォルダーの情報を表示する
TOCTitle: Select a folder and display folder information
ms:assetid: 737b19bc-1efd-4ddb-86d0-72b3ab8eaf8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184616(v=office.15)
ms:contentKeyID: 55119859
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41dc96f26e7e0040467096731cb16ae7c0c08f74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316038"
---
# <a name="select-a-folder-and-display-folder-information"></a><span data-ttu-id="fd2dd-102">フォルダーを選択してフォルダーの情報を表示する</span><span class="sxs-lookup"><span data-stu-id="fd2dd-102">Select a folder and display folder information</span></span>

<span data-ttu-id="fd2dd-103">この例では、指定したフォルダー一覧からユーザーが選択したフォルダーについての情報をプログラムで表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-103">This example shows how to programmatically display information about a folder that a user selects from a specified folder list.</span></span>

## <a name="example"></a><span data-ttu-id="fd2dd-104">例</span><span class="sxs-lookup"><span data-stu-id="fd2dd-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fd2dd-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fd2dd-106">次のコード例の ShowFolderInfo では、[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) メソッドを使用して **[フォルダーの選択]** ダイアログ ボックスをユーザーに表示し、ユーザーがフォルダーを選択するまで待機します。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-106">In the following code example, ShowFolderInfo uses the [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object to display a **Select Folder** dialog box to the user, and waits for the user to select a folder.</span></span> <span data-ttu-id="fd2dd-107">ユーザーがフォルダーを選択すると、その [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\))、[StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\))、[UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\))、[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\))、[CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\))、[Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\))、および [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) プロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-107">Once the user selects a folder, its [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\)), [StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\)), [UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\)), [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\)), [CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\)), [Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\)), and [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) properties are displayed.</span></span> <span data-ttu-id="fd2dd-108">その後、[GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) メソッドを呼び出し、新しい [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトを作成して、フォルダーを表示します。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-108">The example then calls the [GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) method to create a new [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object and display the folder.</span></span>

<span data-ttu-id="fd2dd-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fd2dd-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fd2dd-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd2dd-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void ShowFolderInfo()
{
    Outlook.Folder folder =
        Application.Session.PickFolder()
        as Outlook.Folder;
    if (folder != null)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Folder EntryID:");
        sb.AppendLine(folder.EntryID);
        sb.AppendLine();
        sb.AppendLine("Folder StoreID:");
        sb.AppendLine(folder.StoreID);
        sb.AppendLine();
        sb.AppendLine("Unread Item Count: "
            + folder.UnReadItemCount);
        sb.AppendLine("Default MessageClass: "
            + folder.DefaultMessageClass);
        sb.AppendLine("Current View: "
            + folder.CurrentView.Name);
        sb.AppendLine("Folder Path: "
            + folder.FolderPath);
        MessageBox.Show(sb.ToString(),
            "Folder Information",
            MessageBoxButtons.OK,
            MessageBoxIcon.Information);
        Outlook.Folder folderFromID =
            Application.Session.GetFolderFromID(
            folder.EntryID, folder.StoreID)
            as Outlook.Folder;
        folderFromID.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="fd2dd-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="fd2dd-112">See also</span></span>

- [<span data-ttu-id="fd2dd-113">フォルダー</span><span class="sxs-lookup"><span data-stu-id="fd2dd-113">Folders</span></span>](folders.md)

