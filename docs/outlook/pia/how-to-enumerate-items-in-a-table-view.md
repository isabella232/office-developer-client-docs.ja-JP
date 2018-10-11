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
# <a name="enumerate-items-in-a-table-view"></a><span data-ttu-id="35b17-102">表ビューのアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="35b17-102">Enumerate items in a table view</span></span>

<span data-ttu-id="35b17-103">この例では、[GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) メソッドを使用して表ビューのアイテムを列挙します。</span><span class="sxs-lookup"><span data-stu-id="35b17-103">This example enumerates items in a table view by using the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="35b17-104">例</span><span class="sxs-lookup"><span data-stu-id="35b17-104">Example</span></span>

<span data-ttu-id="35b17-p101">次のコード例では、受信トレイ フォルダーの現在のビューから [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを取得します。その後、アクティブなエクスプローラーの現在のフォルダーを受信トレイに設定し、受信トレイの現在のビューが表ビューであることを確認します。現在のビューが表ビューである場合は、 [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) メソッドを呼び出して、返された **Table** の各行で表される各アイテムを表示します。</span><span class="sxs-lookup"><span data-stu-id="35b17-p101">The following code example obtains a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object from the current view of the Inbox folder. The code example sets the current folder of the active explorer to the Inbox, and then checks that the current view of the Inbox is a table view. If the current view is a table, the code example calls the [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method and displays each item represented by each row in the returned **Table**.</span></span>

<span data-ttu-id="35b17-108">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="35b17-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="35b17-109">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35b17-109">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="35b17-110">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="35b17-110">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="35b17-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="35b17-111">See also</span></span>

- [<span data-ttu-id="35b17-112">ビュー</span><span class="sxs-lookup"><span data-stu-id="35b17-112">Views</span></span>](views.md)

