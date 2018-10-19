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
# <a name="search-and-obtain-items-in-an-aggregated-view"></a><span data-ttu-id="17b7f-102">集計ビュー内のアイテムを検索して取得する</span><span class="sxs-lookup"><span data-stu-id="17b7f-102">Search and Obtain Items in an Aggregated View</span></span>

<span data-ttu-id="17b7f-103">この例では、複数のフォルダーおよびストアにあるアイテムを検索し、それらのアイテムを集計テーブル ビューに返す方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-103">This example shows how to search for items in multiple folders and stores and to return those items in an aggregated table view.</span></span>

## <a name="example"></a><span data-ttu-id="17b7f-104">例</span><span class="sxs-lookup"><span data-stu-id="17b7f-104">Example</span></span>

<span data-ttu-id="17b7f-p101">[TableView](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) オブジェクトの [GetTable()](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) メソッドは、同じストア内の 1 つ以上のフォルダーまたは複数のストアにあるアイテムが含まれる [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを集計ビューに返すことができます。これは、検索 (ストア内の全メール アイテムの検索など) の結果返されるアイテムを操作する場合に特に役立ちます。このトピックでは、現在のユーザーが上司から受信した重要とマークされている全アイテムを **クイック検索**で検索し、検索結果の各アイテムの件名を表示する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-p101">The [GetTable()](https://msdn.microsoft.com/library/ff184699\(v=office.15\)) method of the [TableView](https://msdn.microsoft.com/library/bb608854\(v=office.15\)) object can return, in an aggregated view, a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object that contains items from one or more folders in the same store or spanning over multiple stores. This is particularly useful when you want to access items returned from a search (for example, a search on all mail items in a store). This topic shows an example of how to use **Instant Search** to search for all items received from the manager of the current user that are marked important, and then display the subject of each search result.</span></span>

<span data-ttu-id="17b7f-108">以下のコード例の **GetItemsInView** メソッドは、現在のユーザーの主要な配信ストア アカウントが Exchange アカウントかどうか、現在のユーザーに上司がいるかどうか、およびセッションの既定ストアで**クイック検索**を実行できるかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="17b7f-108">In the following code example, the **GetItemsInView** method checks whether the current user’s primary delivery store account is an Exchange account, whether the current user has a manager, and whether **Instant Search** is operational in the default store of the session.</span></span> <span data-ttu-id="17b7f-109">この検索は [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトの [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) メソッドに依存しており、検索結果は **GetTable** メソッドを使用して取得するため、**GetItemsInView** では、**Explorer** オブジェクトを作成し、このオブジェクト内の受信トレイを表示し、これを使用して検索をセットアップします。</span><span class="sxs-lookup"><span data-stu-id="17b7f-109">Because the search relies on the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object, and the search result is obtained by using the **GetTable** method, **GetItemsInView** creates an **Explorer** object, displays the Inbox in this object, and uses it to set up the search.</span></span> 

<span data-ttu-id="17b7f-110">**GetItemsInView** では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) 型の全フォルダーで、現在のユーザーの上司から受信し、重要とマークされているアイテムを検索します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-110">**GetItemsInView** searches all folders of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) type for items from the current user's manager that are marked as important.</span></span> <span data-ttu-id="17b7f-111">**GetItemsInView** では、[Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) メソッドを呼び出した後、検索結果が Explorer に表示されます。検索結果には、他のフォルダーやストアにあるアイテムも含め、検索条件と一致するアイテムが含まれます。</span><span class="sxs-lookup"><span data-stu-id="17b7f-111">After **GetItemsInView** calls the [Search](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method, any search results are displayed in the Explorer, including items from other folders and stores that meet the search criteria.</span></span> <span data-ttu-id="17b7f-112">**GetItemsInView** は、この検索結果のエクスプローラー ビューが含まれる **TableView** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-112">**GetItemsInView** gets a **TableView** object that contains this explorer view of the search results.</span></span> <span data-ttu-id="17b7f-113">次に、**GetItemsInView** はこの **TableView** オブジェクトの **GetTable** メソッドを使用して、検索で返された集計アイテムを含む **Table** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-113">By using the **GetTable** method of this **TableView** object, **GetItemsInView** then gets a **Table** object that contains the aggregated items returned from the search.</span></span> <span data-ttu-id="17b7f-114">最後に、**GetItemsInView** は、検索結果の各アイテムを表す **Table** オブジェクトの各行から、件名列を表示します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-114">Finally **GetItemsInView** displays the subject column of each row of the **Table** object that represents an item in the search results.</span></span>

<span data-ttu-id="17b7f-115">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="17b7f-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="17b7f-116">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="17b7f-116">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="17b7f-117">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="17b7f-117">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="17b7f-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="17b7f-118">See also</span></span>

- [<span data-ttu-id="17b7f-119">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="17b7f-119">Search and Filter</span></span>](search-and-filter.md)

