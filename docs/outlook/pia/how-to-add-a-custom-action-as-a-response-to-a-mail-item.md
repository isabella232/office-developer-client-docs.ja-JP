---
title: メール アイテムへの返信として行うカスタム アクションを追加する
TOCTitle: Add a custom action as a response to a mail item
ms:assetid: 99e8ba6b-9c47-4b10-968b-436b08d199ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424474(v=office.15)
ms:contentKeyID: 55119870
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a6a82b02d357f86ca37d3ec4987ea6323d6d59cb
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722579"
---
# <a name="add-a-custom-action-as-a-response-to-a-mail-item"></a><span data-ttu-id="bf6b6-102">メール アイテムへの返信として行うカスタム アクションを追加する</span><span class="sxs-lookup"><span data-stu-id="bf6b6-102">Add a custom action as a response to a mail item</span></span>

<span data-ttu-id="bf6b6-103">この例では、[Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) コレクションの [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) メソッドを使用して、電子メール アイテムへの返信として実行するカスタム アクションの追加方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-103">This example shows how to add custom actions as a response to an email item by using the [Add()](https://msdn.microsoft.com/library/bb612077\(v=office.15\)) method of the [Actions](https://msdn.microsoft.com/library/bb611963\(v=office.15\)) collection.</span></span>

## <a name="example"></a><span data-ttu-id="bf6b6-104">例</span><span class="sxs-lookup"><span data-stu-id="bf6b6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bf6b6-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="bf6b6-106">カスタム アクションをプログラムで作成して、電子メールの返信のリボン (**[メッセージ]** タブの **[アクション]** グループ) に表示できます。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-106">You can create custom actions programmatically to appear on the ribbon in the **Actions** group on the **Message** tab in an email response.</span></span> <span data-ttu-id="bf6b6-107">次のコード例の ReplyWithVoiceMail では、"Reply with Voice Mail" という名前のカスタムアクションを作成して、インスペクター コマンド バーに追加します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-107">In the following code example, ReplyWithVoiceMail creates and adds a custom action named “Reply with Voice Mail” to the inspector command bar.</span></span> <span data-ttu-id="bf6b6-108">ReplyWithVoiceMail では、最初に [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) オブジェクトを取得して、その **MailItem** に関連付けられた **Actions** コレクションの **Add** メソッドを呼び出すことで、[Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-108">ReplyWithVoiceMail first gets a [\_MailItem](https://msdn.microsoft.com/library/bb610623\(v=office.15\)) object and then creates an [Action](https://msdn.microsoft.com/library/bb646971\(v=office.15\)) object by calling the **Add** method of the **Actions** collection that is associated with the **MailItem**.</span></span> <span data-ttu-id="bf6b6-109">その後、**Action** オブジェクトの [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) プロパティを "Reply with Voice Mail" に設定します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-109">It then sets the [Name](https://msdn.microsoft.com/library/bb624053\(v=office.15\)) property of the **Action** object to “Reply with Voice Mail”.</span></span> <span data-ttu-id="bf6b6-110">[ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\))、[ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\))、[CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\))、および [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) の各プロパティも設定します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-110">The [ReplyStyle](https://msdn.microsoft.com/library/bb624278\(v=office.15\)), [ResponseStyle](https://msdn.microsoft.com/library/bb622491\(v=office.15\)), [CopyLike](https://msdn.microsoft.com/library/bb624213\(v=office.15\)), and [MessageClass](https://msdn.microsoft.com/library/bb624391\(v=office.15\)) properties are also set.</span></span> <span data-ttu-id="bf6b6-111">最後に、**MailItem** を保存します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-111">Finally, the **MailItem**is saved.</span></span>


> [!NOTE]
> <span data-ttu-id="bf6b6-112">デザイン時に Outlook のフォーム デザイナーを使用してカスタム アクションを追加することもできます。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-112">You can also add custom actions at design time by using the Outlook Forms Designer.</span></span>


<span data-ttu-id="bf6b6-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bf6b6-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bf6b6-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bf6b6-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;

    private void ReplyWithVoiceMail()
    {
        Outlook.MailItem mail = (Outlook.MailItem)Application.ActiveInspector().CurrentItem;
        Outlook.Action action = mail.Actions.Add();
        action.Name = “Reply with Voice Mail”;
        action.ReplyStyle = Outlook.OlActionReplyStyle.olUserPreference;
        action.ResponseStyle = Outlook.OlActionResponseStyle.olOpen;
        action.CopyLike = Outlook.OlActionCopyLike.olReply;
        action.MessageClass = “IPM.Post.Voice Message”;
        mail.Save();
    }
```

## <a name="see-also"></a><span data-ttu-id="bf6b6-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="bf6b6-116">See also</span></span>

- [<span data-ttu-id="bf6b6-117">メール</span><span class="sxs-lookup"><span data-stu-id="bf6b6-117">Mail</span></span>](mail.md)

