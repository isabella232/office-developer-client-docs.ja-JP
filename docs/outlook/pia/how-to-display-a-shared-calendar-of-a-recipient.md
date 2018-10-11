---
title: 受信者の共有の予定表を表示する
TOCTitle: Display a shared calendar of a recipient
ms:assetid: 3dcfec17-c836-4bd0-a177-33c911a94b1f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184606(v=office.15)
ms:contentKeyID: 55119825
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 10101a3eff1b0507c1fe562f175bace7026143fb
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406884"
---
# <a name="display-a-shared-calendar-of-a-recipient"></a><span data-ttu-id="91933-102">受信者の共有の予定表を表示する</span><span class="sxs-lookup"><span data-stu-id="91933-102">Display a shared calendar of a recipient</span></span>

<span data-ttu-id="91933-103">この例では、[CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) メソッドと [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) メソッドを使用して、受信者の共有の予定表を表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="91933-103">This example shows how to display a recipient's shared calendar by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) and [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) methods.</span></span>

## <a name="example"></a><span data-ttu-id="91933-104">例</span><span class="sxs-lookup"><span data-stu-id="91933-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="91933-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="91933-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="91933-p101">[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトなどの送信可能なアイテムは、常に [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) プロパティを公開します。このプロパティを使用することで、送信可能なアイテムの [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションにアクセスできます。アイテムの [Recipients](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) コレクションにバインドされていない **Recipient** オブジェクトを作成するには、 [NameSpace](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) オブジェクトの [CreateRecipient(String)](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) メソッドを使用します。次に、このバインドされていない **Recipient** オブジェクトを [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) メソッドに渡すと、このメソッドから共有の Exchange フォルダーが返されます。これで、共有の Exchange フォルダーを開き、エクスプローラー ウィンドウにそのフォルダーを表示することができます。 GetSharedDefaultFolder は、代理人が委任元のフォルダーへのアクセスを許可されている Exchange 代理シナリオで使用します。 **Recipient** オブジェクトは、 GetSharedDefaultFolder メソッドに渡す前に解決しておく必要があります。 **Recipient** オブジェクトを解決するには、そのオブジェクトの [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="91933-p101">Sendable items such as [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) objects always expose the [Recipients](https://msdn.microsoft.com/library/bb646686\(v=office.15\)) property which, in turn, enables you to access the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection for the sendable item. To create a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object that is not bound to the **Recipients** collection of an item, use the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object. Then pass this unbound **Recipient** object to the [GetSharedDefaultFolder(Recipient, OlDefaultFolders)](https://msdn.microsoft.com/library/bb644850\(v=office.15\)) method, which returns a shared Exchange folder. You can then open the shared Exchange folder and display that folder in an explorer window. GetSharedDefaultFolder is used in Exchange delegate scenarios where the delegate has permission to access the folder of the delegator. Before you pass the **Recipient** object to the GetSharedDefaultFolder method, you must resolve it. To resolve a **Recipient** object, call its [Resolve()](https://msdn.microsoft.com/library/bb624165\(v=office.15\)) method.</span></span>

<span data-ttu-id="91933-p102">次のコード例では、DisplayManagerCalendar が、**CreateRecipient** と **GetSharedDefaultFolder** を呼び出して、現在のユーザーのマネージャーの予定表フォルダーを開き、表示します。ユーザーにマネージャーの予定表フォルダーを開く権限がない、またはエラーが発生すると、通知ダイアログ ボックスが表示されます。</span><span class="sxs-lookup"><span data-stu-id="91933-p102">In the following code example, DisplayManagerCalendar opens and displays the Calendar folder of the current user’s manager by calling **CreateRecipient** and **GetSharedDefaultFolder**. An alert dialog box is displayed if the user does not have permission to open the manager’s Calendar folder or an error occurs.</span></span>


> [!NOTE]
> <span data-ttu-id="91933-115">**Namespace** オブジェクトの **CreateRecipient** メソッド、または **Recipients** コレクションの [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) メソッドを使用して **Recipient** オブジェクトを作成する場合は、受信者の名前を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91933-115">When you create a **Recipient** object by using the **CreateRecipient** method of the **Namespace** object or the [Add(String)](https://msdn.microsoft.com/library/bb612668(v=office.15)) method of the **Recipients** collection, you must provide a recipient name. The Recipient is then resolved against this name. A recipient name can take any of the following formats: >  Display name >  Alias >  Simple Mail Transfer Protocol (SMTP) address</span></span> <span data-ttu-id="91933-116">**Recipient** は、この名前に対して解決されます。</span><span class="sxs-lookup"><span data-stu-id="91933-116">The **Recipient** is then resolved against this name.</span></span> <span data-ttu-id="91933-117">受信者の名前は、次のいずれかの形式をにすることができます。</span><span class="sxs-lookup"><span data-stu-id="91933-117">A recipient name can take any of the following formats:</span></span>
> - <span data-ttu-id="91933-118">表示名</span><span class="sxs-lookup"><span data-stu-id="91933-118">Display name</span></span>
> - <span data-ttu-id="91933-119">エイリアス</span><span class="sxs-lookup"><span data-stu-id="91933-119">Alias</span></span>
> - <span data-ttu-id="91933-120">簡易メール転送プロトコル (SMTP) アドレス</span><span class="sxs-lookup"><span data-stu-id="91933-120">Simple Mail Transfer Protocol (SMTP) address</span></span>

<span data-ttu-id="91933-121">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="91933-121">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="91933-122">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91933-122">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="91933-123">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="91933-123">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void DisplayManagerCalendar()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.Recipient recip =
                Application.Session.CreateRecipient(manager.Name);
            if (recip.Resolve())
            {
                try
                {
                    Outlook.Folder folder =
                        Application.Session.GetSharedDefaultFolder(
                        recip, Outlook.OlDefaultFolders.olFolderCalendar)
                        as Outlook.Folder;
                    folder.Display();
                }
                catch
                {
                    MessageBox.Show("Could not open manager's calendar.",
                        "GetSharedDefaultFolder Example",
                        MessageBoxButtons.OK,
                        MessageBoxIcon.Error);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="91933-124">関連項目</span><span class="sxs-lookup"><span data-stu-id="91933-124">See also</span></span>

- [<span data-ttu-id="91933-125">予定表</span><span class="sxs-lookup"><span data-stu-id="91933-125">Calendar</span></span>](calendar.md)

