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
# <a name="select-a-folder-and-display-folder-information"></a>フォルダーを選択してフォルダーの情報を表示する

この例では、指定したフォルダー一覧からユーザーが選択したフォルダーについての情報をプログラムで表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード例の ShowFolderInfo では、[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [PickFolder()](https://msdn.microsoft.com/library/bb623484\(v=office.15\)) メソッドを使用して **[フォルダーの選択]** ダイアログ ボックスをユーザーに表示し、ユーザーがフォルダーを選択するまで待機します。 ユーザーがフォルダーを選択すると、その [EntryID](https://msdn.microsoft.com/library/bb646192\(v=office.15\))、[StoreID](https://msdn.microsoft.com/library/bb612609\(v=office.15\))、[UnReadItemCount](https://msdn.microsoft.com/library/bb610138\(v=office.15\))、[DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\))、[CurrentView](https://msdn.microsoft.com/library/bb612411\(v=office.15\))、[Name](https://msdn.microsoft.com/library/bb623727\(v=office.15\))、および [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) プロパティを表示します。 その後、[GetFolderFromID](https://msdn.microsoft.com/library/bb647784\(v=office.15\)) メソッドを呼び出し、新しい [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトを作成して、フォルダーを表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [フォルダー](folders.md)

