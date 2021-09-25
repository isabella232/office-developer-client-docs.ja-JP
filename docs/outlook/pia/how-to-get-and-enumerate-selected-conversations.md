---
title: 選択されたスレッドを取得して列挙する
TOCTitle: Get and enumerate selected conversations
ms:assetid: 835312ea-2b29-49a5-b128-f69cf8d4427c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184621(v=office.15)
ms:contentKeyID: 55119833
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 16b766110a2a5bcb80a1653edd4a4bc37c728d9a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560537"
---
# <a name="get-and-enumerate-selected-conversations"></a>選択されたスレッドを取得して列挙する

この例では、[GetSelection(OlSelectionContents)](https://msdn.microsoft.com/library/ff185002\(v=office.15\)) メソッドを使用して、選択されたスレッドを取得して列挙します。

## <a name="example"></a>例

Microsoft Outlook では、受信トレイ内のアイテムをスレッド別に表示するように設定できます。ユーザーが受信トレイで選択を行った場合、プログラムで選択項目を取得でき、これにはスレッドの見出しとアイテムも含まれます。このトピックのコード例では、受信トレイ内の選択項目を取得し、選択されている各スレッドのメール アイテムを列挙する方法を示します。

この例には 1 つのメソッド DemoConversationHeadersFromSelectio が含まれます。 このメソッドは、現在のビューを受信トレイに設定した後、現在のビューがスレッドを日付順に表示している表ビューかどうかを調べます。 選択されているすべての [ConversationHeader](https://msdn.microsoft.com/library/ff184727\(v=office.15\)) オブジェクトを含む選択項目を取得するために、DemoConversationHeadersFromSelection では [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) オブジェクトの **GetSelection** メソッドを使用し、引数として [olConversationHeaders](https://msdn.microsoft.com/library/ff184867\(v=office.15\)) 定数を指定します。 スレッドの見出しが選択されている場合、DemoConversationHeadersFromSelection は [SimpleItems](https://msdn.microsoft.com/library/ff184992\(v=office.15\)) オブジェクトを使用して、選択されている各スレッドのアイテムを列挙し、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトで表されるこれらのスレッド アイテムの件名を表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [会話](conversations.md)

