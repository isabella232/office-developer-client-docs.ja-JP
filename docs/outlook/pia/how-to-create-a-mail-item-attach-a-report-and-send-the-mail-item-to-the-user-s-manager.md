---
title: メール アイテムを作成し、レポートを添付して、ユーザーの上司にメール アイテムを送信する
TOCTitle: Create a mail item, attach a report, and send the mail item to the user's manager
ms:assetid: 15c26c3b-5e86-4e28-92c5-7389572521da
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644320(v=office.15)
ms:contentKeyID: 55119866
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 32c40e1fbda3f0f851b52d29c073d95a5d636620
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349561"
---
# <a name="create-a-mail-item-attach-a-report-and-send-the-mail-item-to-the-users-manager"></a><span data-ttu-id="7598c-102">メール アイテムを作成し、レポートを添付して、ユーザーの上司にメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="7598c-102">Create a mail item, attach a report, and send the mail item to the user's manager</span></span>

<span data-ttu-id="7598c-103">この例では、添付ファイルを持つメール アイテムを作成し、ユーザーの上司宛てに送信します。</span><span class="sxs-lookup"><span data-stu-id="7598c-103">This example creates a mail item that has an attachment, and then sends the mail item to the user's manager.</span></span>

## <a name="example"></a><span data-ttu-id="7598c-104">例</span><span class="sxs-lookup"><span data-stu-id="7598c-104">Example</span></span>

<span data-ttu-id="7598c-p101">この例は、Microsoft Exchange Server アカウントを対象とする場合に限り、適切に動作します。Active Directory ディレクトリ サービスでユーザーと上司の関係が設定されていることが必要です。この例では、[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを使用して [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを呼び出すことによって、現在のユーザーの上司を判別します。</span><span class="sxs-lookup"><span data-stu-id="7598c-p101">This example runs correctly only against a Microsoft Exchange Server account. A manager relationship for users must be established in the Active Directory directory service. The example uses the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object to determine the current user's manager by calling the [GetExchangeUserManager](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method.</span></span>

<span data-ttu-id="7598c-108">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7598c-108">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="7598c-109">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7598c-109">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="7598c-110">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="7598c-110">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub SendSalesReport()
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.Subject = "Quarterly Sales Report FY06 Q4"
    Dim currentUser As Outlook.AddressEntry = _
        Application.Session.CurrentUser.AddressEntry
    If currentUser.Type = "EX" Then
        Dim manager As Outlook.ExchangeUser = _
            currentUser.GetExchangeUser().GetExchangeUserManager()
        ' Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress)
        mail.Recipients.ResolveAll()
        mail.Attachments.Add("c:\sales reports\fy06q4.xlsx", _
            Outlook.OlAttachmentType.olByValue)
        mail.Send()
    End If
End Sub
```


```csharp
private void SendSalesReport()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Quarterly Sales Report FY06 Q4";
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        // Add recipient using display name, alias, or smtp address
        mail.Recipients.Add(manager.PrimarySmtpAddress);
        mail.Recipients.ResolveAll();
        mail.Attachments.Add(@"c:\sales reports\fy06q4.xlsx",
            Outlook.OlAttachmentType.olByValue, Type.Missing,
            Type.Missing);
        mail.Send();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="7598c-111">関連項目</span><span class="sxs-lookup"><span data-stu-id="7598c-111">See also</span></span>

- [<span data-ttu-id="7598c-112">メール</span><span class="sxs-lookup"><span data-stu-id="7598c-112">Mail</span></span>](mail.md)

