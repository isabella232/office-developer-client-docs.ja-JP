---
title: Hotmail アカウントを使用してメール アイテムを送信する
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 008f66ff1a43f90e756900c467ba6c086829b769
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331165"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a><span data-ttu-id="cb1f2-102">Hotmail アカウントを使用してメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="cb1f2-102">Send a mail item by using a Hotmail account</span></span>

<span data-ttu-id="cb1f2-103">この例では、Windows Live Hotmail アカウントを使用してメール アイテムを送信するために、[SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) プロパティを使用しています。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-103">This example uses the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property to send a mail item by using a Windows Live Hotmail account.</span></span>

## <a name="example"></a><span data-ttu-id="cb1f2-104">例</span><span class="sxs-lookup"><span data-stu-id="cb1f2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="cb1f2-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="cb1f2-106">プロファイルでは、1 つ以上の電子メール アカウントを定義します。それぞれの電子メール アカウントは特定の種類 (Microsoft Exchange Server や Post Office Protocol 3 (POP3) など) に関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-106">A profile defines one or more email accounts, and each email account is associated with a server of a specific type, such as Microsoft Exchange Server or Post Office Protocol 3 (POP3).</span></span> <span data-ttu-id="cb1f2-107">プロファイルには複数のアカウントが含まれていることがあるため、アイテムの送信に使用する電子メール アカウントを指定してから、そのアカウントを表す [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-107">Because you may have multiple accounts in your profile, you must specify which email account you want to use to send the item, and then obtain an [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to represent it.</span></span>

<span data-ttu-id="cb1f2-108">次のコード例では、旅程表が添付されたメッセージを作成してから、Windows Live Hotmail アカウントを使用して送信します。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-108">In the following code example, a message is created with an attached itinerary and then sent by using a Windows Live Hotmail account.</span></span> <span data-ttu-id="cb1f2-109">この Hotmail 電子メール アカウントは、ユーザーのプロファイルに含まれる **Account** オブジェクトとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-109">The Hotmail email account is used as the **Account** object in the user’s profile.</span></span> <span data-ttu-id="cb1f2-110">その後、SendUsingAccount プロパティをそのアカウントに設定して、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-110">The code example then sets the SendUsingAccount property to that Account and calls the [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) method from the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span>

<span data-ttu-id="cb1f2-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="cb1f2-112">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="cb1f2-113">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cb1f2-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a><span data-ttu-id="cb1f2-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="cb1f2-114">See also</span></span>

- [<span data-ttu-id="cb1f2-115">アカウント</span><span class="sxs-lookup"><span data-stu-id="cb1f2-115">Accounts</span></span>](accounts.md)

