---
title: 現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する
TOCTitle: Create a sendable item for a specific account based on the current folder
ms:assetid: 665ebdc5-2912-4d85-ac40-835c9ef9a439
ms:contentKeyID: 55119796
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 076677ed2eeedb269ddddc3bee201a162196db0c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405764"
---
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a><span data-ttu-id="42baa-102">現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="42baa-102">Create a Sendable Item for a Specific Account Based on the Current Folder</span></span>

<span data-ttu-id="42baa-103">このトピックには、送信可能な電子メール アイテムと会議出席依頼を作成する方法と、現在のフォルダーに基づく特定のアカウントを使用してそれらを送信する方法を示す 2 つのコード例が含まれています。</span><span class="sxs-lookup"><span data-stu-id="42baa-103">This topic contains two code examples that show how to create a sendable e-mail item and meeting request, and then how to send them by using a specific account that is based on the current folder.</span></span>

## <a name="example"></a><span data-ttu-id="42baa-104">例</span><span class="sxs-lookup"><span data-stu-id="42baa-104">Example</span></span>

<span data-ttu-id="42baa-105">[Application](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) オブジェクトの [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) メソッドを使用して Outlook アイテムを作成する場合、アイテムは、そのセッションの標準アカウントに対して作成されます。</span><span class="sxs-lookup"><span data-stu-id="42baa-105">When you use the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method of the [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object to create an Outlook item, the item is created for the primary account for that session.</span></span> <span data-ttu-id="42baa-106">プロファイルに複数のアカウントが定義されているセッションでは、特定の IMAP アカウント、POP アカウント、または Exchange アカウントに対してアイテムを作成できます。</span><span class="sxs-lookup"><span data-stu-id="42baa-106">In a session where multiple accounts are defined in the profile, you can create an item for a specific IMAP, POP, or Exchange account.</span></span> 

<span data-ttu-id="42baa-107">ユーザー インターフェイスを使用 (例えば、[**新しいメール**] または [**新しい会議**] をクリック) して送信可能なアイテムを作成するときに現在のプロファイルに複数のアカウントがある場合、インスペクターは新しいメールまたは会議出席依頼を作成モードで表示し、それらのアイテムの送信元アカウントを選択することができます。</span><span class="sxs-lookup"><span data-stu-id="42baa-107">If there are multiple accounts in the current profile and you create a sendable item in the user interface, for example, by clicking **New E-mail** or **New Meeting**, an inspector displays a new mail item or meeting request in compose mode, and then you can select the account from which to send the item.</span></span> 

<span data-ttu-id="42baa-108">このトピックでは、プログラムを使用して送信可能アイテムを特定の送信元アカウントで作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="42baa-108">This topic shows how to programmatically create a sendable item and send it by using a specific sending account.</span></span> <span data-ttu-id="42baa-109">このトピックには、アクティブなエクスプローラー内の現在のフォルダーによって判別される特定のアカウントに対する [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) と [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) を作成する方法を示す 2 つのコード例があります。</span><span class="sxs-lookup"><span data-stu-id="42baa-109">The topic has two code examples that show how to create a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) and an [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) for a specific account that is determined by the current folder in the active explorer.</span></span>

<span data-ttu-id="42baa-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="42baa-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="42baa-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="42baa-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="42baa-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="42baa-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="42baa-113">1 番目の方法では、CreateMailItemFromAccount はまず、現在のフォルダーのストア ([Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) プロパティから取得) をセッションの [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) コレクションで定義されている各アカウントの既定の配信ストア ([DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) プロパティで取得) と照合することにより、適切なアカウントを識別します。</span><span class="sxs-lookup"><span data-stu-id="42baa-113"> matches the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained with the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="42baa-114">CreateMailItemFromAccount は **MailItem** を作成します。</span><span class="sxs-lookup"><span data-stu-id="42baa-114">CreateMailItemFromAccount then creates the **MailItem**.</span></span> 

<span data-ttu-id="42baa-115">アイテムをアカウントに関連付けるために、CreateMailItemFromAccount は account.CurrentUser.AddressEntry のプロパティを**MailItem**の[Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) プロパティとして設定することによりアカウントのユーザーをアイテムの送信者として割り当てます。</span><span class="sxs-lookup"><span data-stu-id="42baa-115">To associate the item with the account, CreateMailItemFromAccount assigns the user of the account as the sender of the item by setting the account.CurrentUser.AddressEntry property to the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem**.</span></span> <span data-ttu-id="42baa-116">Sender プロパティの割り当て作業は大事なステップです。送信者を指定しない場合、 既定でプライマリ アカウントに **MailItem** が作成されます。</span><span class="sxs-lookup"><span data-stu-id="42baa-116">Assigning the Sender property is the important step; if you do not specify the sender, the **MailItem** is created for the primary account by default.</span></span> <span data-ttu-id="42baa-117">メソッドの最後で、CreateMailItemFromAccount は **MailItem** を表示します。</span><span class="sxs-lookup"><span data-stu-id="42baa-117">At the end of the method, CreateMailItemFromAccount displays the **MailItem**.</span></span> <span data-ttu-id="42baa-118">なお、現在のフォルダーが配信ストアにない場合は、CreateMailItemFromAccount は現在のセッションのプライマリ アカウントに **MailItem** を作成します。</span><span class="sxs-lookup"><span data-stu-id="42baa-118">Note that if the current folder is not on a delivery store, CreateMailItemFromAccount creates the **MailItem** for the primary account for the session.</span></span>

```csharp
private void CreateMailItemFromAccount()
{
    Outlook.AddressEntry addrEntry = null;
    // Get the Store for CurrentFolder.
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder 
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    // Enumerate accounts to find
    // account.DeliveryStore for store.
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID == 
            store.StoreID)
        {
            addrEntry =
                account.CurrentUser.AddressEntry;
            break;
        }
    }
    // Create MailItem.
    Outlook.MailItem mail =
        Application.CreateItem(
        Outlook.OlItemType.olMailItem)
        as Outlook.MailItem;
    if (addrEntry != null)
    {
        // Set Sender property.
        mail.Sender = addrEntry;
        mail.Display(false);
    }
}
```

<span data-ttu-id="42baa-119">2 番目の方法の CreateMeetingRequestFromAccount は CreateMailItemFromAccount と似ていますが、MailItem ではなく AppointmentItem が作成されるという点が違います。</span><span class="sxs-lookup"><span data-stu-id="42baa-119">The next method, CreateMeetingRequestFromAccount, is similar to CreateMailItemFromAccount except that it creates an AppointmentItem instead of a MailItem.</span></span> <span data-ttu-id="42baa-120">CreateMeetingRequestFromAccount はまず、現在のフォルダーのストア ([Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) プロパティから取得) をセッションの Accounts コレクションで定義されている各アカウントの既定の[配信ストア](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) (DeliveryStore プロパティで取得) と照合することにより、適切なアカウントを識別します。</span><span class="sxs-lookup"><span data-stu-id="42baa-120"> matches the store of the current folder (obtained from the Store property) with the default delivery store of each account (obtained with the DeliveryStore property) that is defined in the Accounts collection for the session.</span></span> <span data-ttu-id="42baa-121">CreateMeetingRequestFromAccount はその後に AppointmentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="42baa-121">CreateMeetingRequestFromAccount then creates the AppointmentItem.</span></span> 

<span data-ttu-id="42baa-122">アイテムをアカウントに関連付けるために、CreateMeetingRequestFromAccount は [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを AppointmentItem の [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) プロパティとして設定することにより、そのアカウントをアイテムの送信元アカウントとして割り当てます。</span><span class="sxs-lookup"><span data-stu-id="42baa-122">To associate the item with the account, CreateMeetingRequestFromAccount assigns that account as the item's sending account by setting the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object to the [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) property of the AppointmentItem.</span></span> <span data-ttu-id="42baa-123">SendUsingAccount プロパティの割り当て作業は大事なステップです。アカウントを指定しない場合、 既定でプライマリ アカウントに AppointmentItem が作成されます。</span><span class="sxs-lookup"><span data-stu-id="42baa-123">Assigning the SendUsingAccount property is the important step; if you do not specify the account, the AppointmentItem is created for the primary account by default.</span></span> <span data-ttu-id="42baa-124">メソッドの最後で、CreateMeetingRequestFromAccount は AppointmentItem を表示します。</span><span class="sxs-lookup"><span data-stu-id="42baa-124">At the end of the method, CreateMeetingRequestFromAccount displays the AppointmentItem.</span></span> <span data-ttu-id="42baa-125">なお、現在のフォルダーが配信ストアにない場合は、CreateMeetingRequestFromAccount は現在のセッションのプライマリ アカウントに AppointmentItem を作成します。</span><span class="sxs-lookup"><span data-stu-id="42baa-125">Note that if the current folder is not on a delivery store, CreateMeetingRequestFromAccount creates the AppointmentItem for the primary account for the session.</span></span>

```csharp
private void CreateMeetingRequestFromAccount()
{
    Outlook.Account acct = null;
    Outlook.Folder folder =
        Application.ActiveExplorer().CurrentFolder
        as Outlook.Folder;
    Outlook.Store store = folder.Store;
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        if (account.DeliveryStore.StoreID ==
            store.StoreID)
        {
            acct = account;
            break;
        }
    }
    Outlook.AppointmentItem appt =
        Application.CreateItem(
        Outlook.OlItemType.olAppointmentItem)
        as Outlook.AppointmentItem;
    appt.MeetingStatus = 
        Outlook.OlMeetingStatus.olMeeting;
    if (acct != null)
    {
        // Set SendUsingAccount property.
        appt.SendUsingAccount=acct;
        appt.Display(false);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="42baa-126">関連項目</span><span class="sxs-lookup"><span data-stu-id="42baa-126">See also</span></span>

- [<span data-ttu-id="42baa-127">アカウント</span><span class="sxs-lookup"><span data-stu-id="42baa-127">Accounts</span></span>](accounts.md)

