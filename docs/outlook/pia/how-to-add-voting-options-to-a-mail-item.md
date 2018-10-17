---
title: メール アイテムに投票オプションを追加する
TOCTitle: Add voting options to a mail item
ms:assetid: 0fb209a8-178d-411e-9551-0a72e041fd65
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424466(v=office.15)
ms:contentKeyID: 55119867
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 6a65bdd5086a10b2d6e9803047555a8b052ff38e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407171"
---
# <a name="add-voting-options-to-a-mail-item"></a><span data-ttu-id="c43cb-102">メール アイテムに投票オプションを追加する</span><span class="sxs-lookup"><span data-stu-id="c43cb-102">Add voting options to a mail item</span></span>

<span data-ttu-id="c43cb-103">この例では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) プロパティを使用して、電子メール メッセージに投票オプションを追加する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c43cb-103">This example shows how to use the [VotingOptions](https://msdn.microsoft.com/library/bb652695\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object to add voting options to an e-mail message.</span></span>

## <a name="example"></a><span data-ttu-id="c43cb-104">例</span><span class="sxs-lookup"><span data-stu-id="c43cb-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c43cb-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="c43cb-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="c43cb-p101">メッセージの投票オプションは、メッセージ受信者に選択肢の一覧を示して回答を追跡するために使用します。投票オプションをプログラムで作成するには、値の一覧をセミコロン区切りで記述した文字列を **MailItem** オブジェクトの **VotingOptions** プロパティに設定します。 **VotingOptions** プロパティの値は、受信メッセージのリボンの [ **返信**] グループの [ **投票**] コマンドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="c43cb-p101">Voting options on messages are used to give message recipients a list of choices and to track their responses. To create voting options programmatically, set a string that is a semicolon-delimited list of values for the **VotingOptions** property of a **MailItem** object. The values for the **VotingOptions** property will appear under the **Vote** command in the **Respond** group in the ribbon of the received message.</span></span>

<span data-ttu-id="c43cb-109">次の例の OrderPizza は、新しいメール メッセージに投票オプションを作成します。</span><span class="sxs-lookup"><span data-stu-id="c43cb-109">In the following example,   creates voting options in a new mail message.</span></span> <span data-ttu-id="c43cb-110">OrderPizza は、まず **MailItem** を作成し、**VotingOptions** プロパティを "Cheese; Mushroom; Sausage; Combo; Veg Combo" に設定して、[Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) プロパティを "Pizza Order" に設定します。</span><span class="sxs-lookup"><span data-stu-id="c43cb-110"> first creates a MailItem, and then sets the VotingOptions property to "Cheese; Mushroom; Sausage; Combo; Veg Combo", and the Subject property to "Pizza Order".</span></span> <span data-ttu-id="c43cb-111">"Pizza Order" メッセージを送信すると、受信者には投票オプションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="c43cb-111">When the "Pizza Order" message is sent, the voting options appear to recipients.</span></span> <span data-ttu-id="c43cb-112">回答を受診するたびに、差出人の送信済みアイテム フォルダーのメッセージの **[追跡]** ページに、受診者の選択内容が集計されます。</span><span class="sxs-lookup"><span data-stu-id="c43cb-112">For each response received, the recipient's choice will be tallied on the **Tracking** page of the message in the sender's Sent Items folder.</span></span>

<span data-ttu-id="c43cb-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c43cb-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="c43cb-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c43cb-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="c43cb-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c43cb-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void OrderPizza()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.CreateItem(
            Outlook.OlItemType.olMailItem);
        mail.VotingOptions = “Cheese; Mushroom; Sausage; Combo; Veg Combo;”
        mail.Subject = “Pizza Order”;
        mail.Display(false);
    }
```

## <a name="see-also"></a><span data-ttu-id="c43cb-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="c43cb-116">See also</span></span>

- [<span data-ttu-id="c43cb-117">メール</span><span class="sxs-lookup"><span data-stu-id="c43cb-117">Mail</span></span>](mail.md)
