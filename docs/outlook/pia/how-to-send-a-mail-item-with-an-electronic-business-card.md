---
title: 電子名刺付きのメール アイテムを送信する
TOCTitle: Send a mail item with an electronic business card
ms:assetid: f8aae7f2-85fc-4ed0-9f59-282ede702357
ms:mtpsurl: https://msdn.microsoft.com/library/Bb624312(v=office.15)
ms:contentKeyID: 55119839
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25809fc0d1726c9f56be417ae53fadecc831d62f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704547"
---
# <a name="send-a-mail-item-with-an-electronic-business-card"></a><span data-ttu-id="c39f3-102">電子名刺付きのメール アイテムを送信する</span><span class="sxs-lookup"><span data-stu-id="c39f3-102">Send a mail item with an electronic business card</span></span>

<span data-ttu-id="c39f3-103">この例では、メール アイテムを作成し、電子名刺を検索して、見つかった場合は、電子名刺をメール アイテムに挿入します。</span><span class="sxs-lookup"><span data-stu-id="c39f3-103">This example creates a mail item, looks for an electronic business card, and if it finds one, inserts the electronic business card into the mail item.</span></span>

## <a name="example"></a><span data-ttu-id="c39f3-104">例</span><span class="sxs-lookup"><span data-stu-id="c39f3-104">Example</span></span>

<span data-ttu-id="c39f3-105">電子名刺を挿入するには、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) を呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c39f3-105">To insert an electronic business card, you can call [AddBusinessCard](https://msdn.microsoft.com/library/bb647034\(v=office.15\)) on the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="c39f3-106">このメソッドは、メール アドレスを表す文字列を受け取り、既定の連絡先フォルダーでそのアドレスの [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) を検索します。</span><span class="sxs-lookup"><span data-stu-id="c39f3-106">This method takes a string representing an email address and attempts to find a [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) with that address in the default Contacts folder.</span></span> <span data-ttu-id="c39f3-107">1 つの **ContactItem** にメール アドレスを 3 つまで設定できます。</span><span class="sxs-lookup"><span data-stu-id="c39f3-107">A **ContactItem** can have as many as three email addresses.</span></span> <span data-ttu-id="c39f3-108">連絡先が見つかった場合は、**AddBusinessCard** メソッドを呼び出した後、メッセージをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="c39f3-108">If the contact is found, the example calls the **AddBusinessCard** method, and then displays the message to the user.</span></span>

<span data-ttu-id="c39f3-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c39f3-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c39f3-110">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c39f3-110">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c39f3-111">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c39f3-111">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub AddBusinessCard(ByVal eMailAddress As String)
    Dim mail As Outlook.MailItem = CType(Application.CreateItem( _
        Outlook.OlItemType.olMailItem), Outlook.MailItem)
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML
    Dim contact As Outlook.ContactItem = _
        CType(Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find( _
        "[Email1Address]='" & eMailAddress & "'" & " OR " & _
        "[Email2Address]='" & eMailAddress & "'" + " OR " & _
        "[Email3Address]='" & eMailAddress & "'") _
        , Outlook.ContactItem)
    If (contact Is Nothing) Then
        Return
    End If
    mail.AddBusinessCard(contact)
    mail.Display(False)
End Sub
```


```csharp
private void AddBusinessCard(string eMailAddress)
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.BodyFormat = Outlook.OlBodyFormat.olFormatHTML;
    Outlook.ContactItem contact = Application.Session.
        GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts).Items.Find(
        "[Email1Address]='" + eMailAddress + "'" + " OR " +
        "[Email2Address]='" + eMailAddress + "'" + " OR " +
        "[Email3Address]='" + eMailAddress + "'")
        as Outlook.ContactItem;
    if (contact == null)
    {
        return;
    }
    mail.AddBusinessCard(contact);
    mail.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="c39f3-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="c39f3-112">See also</span></span>

- [<span data-ttu-id="c39f3-113">電子名刺</span><span class="sxs-lookup"><span data-stu-id="c39f3-113">Electronic business cards</span></span>](electronic-business-cards.md)

