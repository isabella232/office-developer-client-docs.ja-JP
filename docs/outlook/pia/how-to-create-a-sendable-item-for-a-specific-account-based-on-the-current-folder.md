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
# <a name="create-a-sendable-item-for-a-specific-account-based-on-the-current-folder"></a>現在のフォルダーに基づいて特定のアカウントの送信可能なアイテムを作成する

このトピックには、送信可能なメール アイテムと会議出席依頼を作成する方法と、現在のフォルダーに基づく特定のアカウントを使用してそれらを送信する方法を示す 2 つのコード例が含まれています。

## <a name="example"></a>例

[Application](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) オブジェクトの [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) メソッドを使用して Outlook アイテムを作成する場合、アイテムは、そのセッションの標準アカウントに対して作成されます。 プロファイルに複数のアカウントが定義されているセッションでは、特定の IMAP アカウント、POP アカウント、または Exchange アカウントに対してアイテムを作成できます。 

ユーザー インターフェイスを使用 (たとえば、[**新しいメール**] または [**新しい会議**] をクリック) して送信可能なアイテムを作成するときに現在のプロファイルに複数のアカウントがある場合、インスペクターは新しいメールまたは会議出席依頼を作成モードで表示し、それらのアイテムの送信元アカウントを選択することができます。 

このトピックでは、プログラムを使用して送信可能なアイテムを特定の送信元アカウントで作成する方法を説明します。 このトピックには、アクティブなエクスプローラー内の現在のフォルダーによって判別される特定のアカウントに対する [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) と [AppointmentItem](https://msdn.microsoft.com/library/bb645611\(v=office.15\)) を作成する方法を示す 2 つのコード例があります。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

1 番目の方法では、CreateMailItemFromAccount はまず、現在のフォルダーのストア ([Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) プロパティから取得) をセッションの [Accounts](https://msdn.microsoft.com/library/bb646328\(v=office.15\)) コレクションで定義されている各アカウントの既定の配信ストア ([DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) プロパティで取得) と照合して、適切なアカウントを識別します。 CreateMailItemFromAccount は **MailItem** を作成します。 

アイテムをアカウントに関連付けるために、CreateMailItemFromAccount は account.CurrentUser.AddressEntry のプロパティを**MailItem**の[Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) プロパティとして設定してアカウントのユーザーをアイテムの送信者として割り当てます。 Sender プロパティの割り当て作業は大事なステップです。送信者を指定しない場合、既定でプライマリ アカウントに **MailItem** が作成されます。 メソッドの最後で、CreateMailItemFromAccount は **MailItem** を表示します。 なお、現在のフォルダーが配信ストアにない場合は、CreateMailItemFromAccount は現在のセッションのプライマリ アカウントに **MailItem** を作成します。

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

2 番目の方法の CreateMeetingRequestFromAccount は CreateMailItemFromAccount と似ていますが、MailItem ではなく AppointmentItem が作成されるという点が違います。 CreateMeetingRequestFromAccount はまず、現在のフォルダーのストア ([Store](https://msdn.microsoft.com/library/bb612742\(v=office.15\)) プロパティから取得) をセッションの Accounts コレクションで定義されている各アカウントの既定の配信ストア ([DeliveryStore](https://msdn.microsoft.com/library/ff185090\(v=office.15\)) プロパティで取得) と照合して、適切なアカウントを識別します。 CreateMeetingRequestFromAccount はその後に AppointmentItem を作成します。 

アイテムをアカウントに関連付けるために、CreateMeetingRequestFromAccount は [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを AppointmentItem の [SendUsingAccount](https://msdn.microsoft.com/library/bb610680\(v=office.15\)) プロパティとして設定して、そのアカウントをアイテムの送信元アカウントとして割り当てます。 SendUsingAccount プロパティの割り当て作業は大事なステップです。アカウントを指定しない場合、既定でプライマリ アカウントに AppointmentItem が作成されます。 メソッドの最後で、CreateMeetingRequestFromAccount は AppointmentItem を表示します。 なお、現在のフォルダーが配信ストアにない場合は、CreateMeetingRequestFromAccount は現在のセッションのプライマリ アカウントに AppointmentItem を作成します。

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

## <a name="see-also"></a>関連項目

- [アカウント](accounts.md)

