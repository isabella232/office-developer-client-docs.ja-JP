---
title: スレッド内のアイテムを取得して表示する
TOCTitle: Get and display items in a conversation
ms:assetid: 8f30a7cb-0949-46d7-bc51-2d93dbb22bf8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184625(v=office.15)
ms:contentKeyID: 55119832
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0fcfe76632c2fda742a85a571d655569dc2fcd33
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349463"
---
# <a name="get-and-display-items-in-a-conversation"></a>スレッド内のアイテムを取得して表示する

この例では、スレッド内のメール アイテムを取得して表示する方法を示します。

## <a name="example"></a>例

次のコード例の DemoConversation では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトを取得してから、[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトの [Store](https://msdn.microsoft.com/library/bb609093\(v=office.15\)) プロパティを使用して **MailItem** オブジェクトのストアを調べます。 その後、DemoConversation では、[IsConversationEnabled](https://msdn.microsoft.com/library/ff185030\(v=office.15\)) プロパティが **true** かどうかを確認します。**true** の場合は、[GetConversation()](https://msdn.microsoft.com/library/ff184974\(v=office.15\)) メソッドを使用して [Conversation](https://msdn.microsoft.com/library/ff184711\(v=office.15\)) オブジェクトを取得します。 **Conversation** オブジェクトが null 参照でない場合は、[GetTable()](https://msdn.microsoft.com/library/ff185184\(v=office.15\)) メソッドを使用して、関連付けられた [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを取得します。このオブジェクトには、スレッド内の各アイテムが格納されています。 

その後、**Table** 内の各アイテムを列挙して、アイテムごとに EnumerateConversation を呼び出して、各アイテムの子ノードにアクセスします。 EnumerateConversation は、**Conversation** オブジェクトを受け取って、[GetChildren(Object)](https://msdn.microsoft.com/library/ff184854\(v=office.15\)) メソッドを使用することで子ノードを取得します。 EnumerateConversation は、子ノードがなくなるまで再帰的に呼び出されます。 その後、スレッド内の各アイテムがユーザーに表示されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
void DemoConversation()
{
    object selectedItem = 
        Application.ActiveExplorer().Selection[1];
    // For this example, you will work only with 
    //MailItem. Other item types such as
    //MeetingItem and PostItem can participate 
    //in Conversation.
    if (selectedItem is Outlook.MailItem)
    {
        // Cast selectedItem to MailItem.
        Outlook.MailItem mailItem =
            selectedItem as Outlook.MailItem; ;
        // Determine store of mailItem.
        Outlook.Folder folder = mailItem.Parent
            as Outlook.Folder;
        Outlook.Store store = folder.Store;
        if (store.IsConversationEnabled == true)
        {
            // Obtain a Conversation object.
            Outlook.Conversation conv =
                mailItem.GetConversation();
            // Check for null Conversation.
            if (conv != null)
            {
                // Obtain Table that contains rows 
                // for each item in Conversation.
                Outlook.Table table = conv.GetTable();
                Debug.WriteLine("Conversation Items Count: " +
                    table.GetRowCount().ToString());
                Debug.WriteLine("Conversation Items from Table:");
                while (!table.EndOfTable)
                {
                    Outlook.Row nextRow = table.GetNextRow();
                    Debug.WriteLine(nextRow["Subject"]
                        + " Modified: "
                        + nextRow["LastModificationTime"]);
                }
                Debug.WriteLine("Conversation Items from Root:");
                // Obtain root items and enumerate Conversation.
                Outlook.SimpleItems simpleItems 
                    = conv.GetRootItems();
                foreach (object item in simpleItems)
                {
                    // In this example, enumerate only MailItem type.
                    // Other types such as PostItem or MeetingItem
                    // can appear in Conversation.
                    if (item is Outlook.MailItem)
                    {
                        Outlook.MailItem mail = item
                            as Outlook.MailItem;
                        Outlook.Folder inFolder =
                            mail.Parent as Outlook.Folder;
                        string msg = mail.Subject
                            + " in folder " + inFolder.Name;
                        Debug.WriteLine(msg);
                    }
                    // Call EnumerateConversation 
                    // to access child nodes of root items.
                    EnumerateConversation(item, conv);
                }
            }
        }
    }
}

void EnumerateConversation(object item,
    Outlook.Conversation conversation)
{
    Outlook.SimpleItems items =
        conversation.GetChildren(item);
    if (items.Count > 0)
    {
        foreach (object myItem in items)
        {
            // In this example, enumerate only MailItem type.
            // Other types such as PostItem or MeetingItem
            // can appear in Conversation.
            if (myItem is Outlook.MailItem)
            {
                Outlook.MailItem mailItem =
                    myItem as Outlook.MailItem;
                Outlook.Folder inFolder =
                    mailItem.Parent as Outlook.Folder;
                string msg = mailItem.Subject
                    + " in folder " + inFolder.Name;
                Debug.WriteLine(msg);
            }
            // Continue recursion.
            EnumerateConversation(myItem, conversation);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [会話](conversations.md)

