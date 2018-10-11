---
title: 表ビューのアイテムを列挙する
TOCTitle: Enumerate items in a table view
ms:assetid: c7d9a667-cfec-49c1-af7a-4c8063991588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184640(v=office.15)
ms:contentKeyID: 55119900
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: fbb3b6aa9bed2e08eb11cb58090233d271e5fed3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406450"
---
# <a name="enumerate-items-in-a-table-view"></a>表ビューのアイテムを列挙する

この例では、[GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) メソッドを使用して表ビューのアイテムを列挙します。

## <a name="example"></a>例

次のコード例では、受信トレイ フォルダーの現在のビューから [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを取得します。その後、アクティブなエクスプローラーの現在のフォルダーを受信トレイに設定し、受信トレイの現在のビューが表ビューであることを確認します。現在のビューが表ビューである場合は、 [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) メソッドを呼び出して、返された **Table** の各行で表される各アイテムを表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoViewGetTable()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder
    // for View.GetTable to work correctly.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType == 
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view = 
            inbox.CurrentView as Outlook.TableView;
        // No arguments needed for View.GetTable.
        Outlook.Table table = view.GetTable();
        Debug.WriteLine("View Count=" 
            + table.GetRowCount().ToString());
        while (!table.EndOfTable)
        {
            // First row in Table.
            Outlook.Row nextRow = table.GetNextRow();
            Debug.WriteLine(nextRow["Subject"]
                + " Modified: "
                + nextRow["LastModificationTime"]);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [ビュー](views.md)

