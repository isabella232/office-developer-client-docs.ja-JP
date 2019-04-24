---
title: 選択されたスレッドを取得して列挙する
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2d71fc1d582abebc8cb00f4885ec5b5ba348228c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320315"
---
# <a name="get-and-enumerate-selected-conversations"></a><span data-ttu-id="b2f17-102">選択されたスレッドを取得して列挙する</span><span class="sxs-lookup"><span data-stu-id="b2f17-102">Get and enumerate selected conversations</span></span>

<span data-ttu-id="b2f17-103">この例では、[GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) メソッドを使用して、選択されたスレッドを取得して列挙します。</span><span class="sxs-lookup"><span data-stu-id="b2f17-103">This example obtains and enumerates selected conversations by using the [GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="b2f17-104">例</span><span class="sxs-lookup"><span data-stu-id="b2f17-104">Example</span></span>

<span data-ttu-id="b2f17-p101">Microsoft Outlook では、受信トレイ内のアイテムをスレッド別に表示するように設定できます。ユーザーが受信トレイで選択を行った場合、プログラムで選択項目を取得でき、これにはスレッドの見出しとアイテムも含まれます。このトピックのコード例では、受信トレイ内の選択項目を取得し、選択されている各スレッドのメール アイテムを列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b2f17-p101">Microsoft Outlook can be set to display items in the Inbox by conversation. If a user makes a selection in the Inbox, you can obtain the selection programmatically, including conversation headers and conversation items. The code example in this topic shows how to obtain a selection in the Inbox and enumerate the mail items in each conversation in the selection.</span></span>

<span data-ttu-id="b2f17-108">この例には 1 つのメソッド DemoConversationHeadersFromSelectio が含まれます。</span><span class="sxs-lookup"><span data-stu-id="b2f17-108">The example contains one method, DemoConversationHeadersFromSelection.</span></span> <span data-ttu-id="b2f17-109">このメソッドは、現在のビューを受信トレイに設定した後、現在のビューがスレッドを日付順に表示している表ビューかどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="b2f17-109">The method sets the current view to the Inbox, and then checks whether the current view is a table view that displays conversations sorted by date.</span></span> <span data-ttu-id="b2f17-110">選択されているすべての [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) オブジェクトを含む選択項目を取得するために、DemoConversationHeadersFromSelection では [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) オブジェクトの **GetSelection** メソッドを使用し、引数として [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) 定数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2f17-110">To obtain a selection, including any selected [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) objects, DemoConversationHeadersFromSelection uses the **GetSelection** method of the [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object, specifying the [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) constant as an argument.</span></span> <span data-ttu-id="b2f17-111">スレッドの見出しが選択されている場合、DemoConversationHeadersFromSelection は [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) オブジェクトを使用して、選択されている各スレッドのアイテムを列挙し、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトで表されるこれらのスレッド アイテムの件名を表示します。</span><span class="sxs-lookup"><span data-stu-id="b2f17-111">If conversation headers are selected, DemoConversationHeadersFromSelection uses the [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) object to enumerate items in each selected conversation, and then displays the subject of those conversation items that are [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects.</span></span>

<span data-ttu-id="b2f17-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2f17-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="b2f17-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b2f17-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="b2f17-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b2f17-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoConversationHeadersFromSelection()
{
    // Obtain Inbox.
    Outlook.Folder inbox =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Set ActiveExplorer.CurrentFolder to Inbox.
    // Inbox must be current folder.
    Application.ActiveExplorer().CurrentFolder = inbox;
    // Ensure that current view is TableView.
    if (inbox.CurrentView.ViewType ==
        Outlook.OlViewType.olTableView)
    {
        Outlook.TableView view =
            inbox.CurrentView as Outlook.TableView;
        if (view.ShowConversationByDate == true)
        {
            Outlook.Selection selection =
                Application.ActiveExplorer().Selection;
            Debug.WriteLine("Selection.Count = " + selection.Count);
            // Call GetSelection to create a Selection object
            // that contains ConversationHeader objects.
            Outlook.Selection convHeaders =
                selection.GetSelection(
                Outlook.OlSelectionContents.olConversationHeaders)
                as Outlook.Selection;
            Debug.WriteLine("Selection.Count (ConversationHeaders) = " 
                + convHeaders.Count);
            if (convHeaders.Count >= 1)
            {
                foreach (Outlook.ConversationHeader convHeader in convHeaders)
                {
                    // Enumerate the items in the ConversationHeader.
                    Outlook.SimpleItems items = convHeader.GetItems();
                    for (int i = 1; i <= items.Count; i++)
                    {
                        // Enumerate only MailItems in this example.
                        if (items[i] is Outlook.MailItem)
                        {
                            Outlook.MailItem mail = 
                                items[i] as Outlook.MailItem;
                            Debug.WriteLine(mail.Subject 
                                + " Received:" + mail.ReceivedTime);
                        }
                    }
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="b2f17-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="b2f17-115">See also</span></span>

- [<span data-ttu-id="b2f17-116">会話</span><span class="sxs-lookup"><span data-stu-id="b2f17-116">Conversations</span></span>](conversations.md)

