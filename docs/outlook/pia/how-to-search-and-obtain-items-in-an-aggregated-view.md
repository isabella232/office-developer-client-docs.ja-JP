---
title: 集計ビュー内のアイテムを検索して取得する
TOCTitle: Search and obtain items in an aggregated view
ms:assetid: 1a875dc8-dd52-4e9c-b292-5f6ba3d7a940
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184592(v=office.15)
ms:contentKeyID: 55119925
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 540557973d395c23d26a87502ed6ba43176a0a3c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407577"
---
# <a name="search-and-obtain-items-in-an-aggregated-view"></a>集計ビュー内のアイテムを検索して取得する

この例では、複数のフォルダーおよびストアにあるアイテムを検索し、それらのアイテムを集計テーブル ビューに返す方法を説明します。

## <a name="example"></a>例

[TableView](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) オブジェクトの [GetTable()](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) メソッドは、同じストア内の 1 つ以上のフォルダーまたは複数のストアにあるアイテムが含まれる [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを集計ビューに返すことができます。これは、検索 (ストア内の全メール アイテムの検索など) の結果返されるアイテムを操作する場合に特に役立ちます。このトピックでは、現在のユーザーが上司から受信した重要とマークされている全アイテムを **クイック検索**で検索し、検索結果の各アイテムの件名を表示する方法について説明します。

以下のコード例の **GetItemsInView** メソッドは、現在のユーザーの主要な配信ストア アカウントが Exchange アカウントかどうか、現在のユーザーに上司がいるかどうか、およびセッションの既定ストアで**クイック検索**を実行できるかどうかを調べます。 この検索は [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトの [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) メソッドに依存しており、検索結果は **GetTable** メソッドを使用して取得するため、**GetItemsInView** では、**Explorer** オブジェクトを作成し、このオブジェクト内の受信トレイを表示し、これを使用して検索をセットアップします。 

**GetItemsInView** では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) 型の全フォルダーで、現在のユーザーの上司から受信し、重要とマークされているアイテムを検索します。 **GetItemsInView** では、[Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) メソッドを呼び出した後、検索結果が Explorer に表示されます。検索結果には、他のフォルダーやストアにあるアイテムも含め、検索条件と一致するアイテムが含まれます。 **GetItemsInView** は、この検索結果のエクスプローラー ビューが含まれる **TableView** オブジェクトを取得します。 次に、**GetItemsInView** はこの **TableView** オブジェクトの **GetTable** メソッドを使用して、検索で返された集計アイテムを含む **Table** オブジェクトを取得します。 最後に、**GetItemsInView** は、検索結果の各アイテムを表す **Table** オブジェクトの各行から、件名列を表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetItemsInView()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;

    // Check whether the current user uses the Exchange Server.
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();

        // Check whether the current user has a manager.
        if (manager != null)
        {
            string managerName = manager.Name;

            // Check whether Instant Search is enabled and 
            // operational in the default store.
            if (Application.Session.DefaultStore.IsInstantSearchEnabled)
            {
                Outlook.Folder inbox =
                    Application.Session.GetDefaultFolder(
                    Outlook.OlDefaultFolders.olFolderInbox);

                // Create a new explorer to display the Inbox as
                // the current folder.
                Outlook.Explorer explorer =
                    Application.Explorers.Add(inbox,
                    Outlook.OlFolderDisplayMode.olFolderDisplayNormal);

                // Make the new explorer visible.
                explorer.Display;

                // Search for items from the manager marked important, 
                // from all folders of the same item type as the current folder, 
                // which is the MailItem item type.
                string searchFor =
                    "from:" + "\"" + managerName 
                    + "\"" + " importance:high";
                explorer.Search(searchFor,
                    Outlook.OlSearchScope.olSearchScopeAllFolders);

                // Any search results are displayed in that new explorer
                // in an aggregated table view.
                Outlook.TableView tableView = 
                    explorer.CurrentView as Outlook.TableView;

                // Use GetTable of that table view to obtain items in that
                // aggregated view in a Table object.
                Outlook.Table table = tableView.GetTable();
                while (!table.EndOfTable)
                {
                    // Then display each row in the Table object
                    // that represents an item in the search results.
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]);
                }
            }
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

