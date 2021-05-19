---
title: 受信者のメール アドレスを取得する
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-get-the-e-mail-address-of-a-recipient?redirectedfrom=MSDN
ms:contentKeyID: 55119879
ms.date: 12/03/2019
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8957cbc92414b0cdac442167a5c9ea025ce318cb
ms.sourcegitcommit: 37080eb0087261320e24e6f067e5f434a812b2d2
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/04/2019
ms.locfileid: "39819337"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="bff5a-102">受信者のメール アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="bff5a-102">Get the email address of a recipient</span></span>

<span data-ttu-id="bff5a-103">この例では、受信者の簡易メール転送プロトコル (SMTP) アドレスを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="bff5a-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="bff5a-104">例</span><span class="sxs-lookup"><span data-stu-id="bff5a-104">Example</span></span>

<span data-ttu-id="bff5a-105">次のコード例の GetSMTPAddressForRecipients メソッドは、入力引数として [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) オブジェクトを受け取り、そのメール アイテムの各受信者の SMTP アドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="bff5a-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.mailitem?redirectedfrom=MSDN&view=outlook-pia) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="bff5a-106">このメソッドでは、最初にメール アイテムに対して指定されている一連の受信者を表す [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) コレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="bff5a-106">The method first retrieves the [Recipients](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipients?redirectedfrom=MSDN&view=outlook-pia) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="bff5a-107">その **Recipients** [コレクション](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia)内の受信者ごとに、その Recipient オブジェクトに対応する [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) オブジェクトを **取得** します。</span><span class="sxs-lookup"><span data-stu-id="bff5a-107">For each [Recipient](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient?redirectedfrom=MSDN&view=outlook-pia) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="bff5a-108">最後に、メソッドは [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor)プロパティを使用して MAPI プロパティの値を取得し、受信者の https://schemas.microsoft.com/mapi/proptag/0x39FE001E PR SMTP **\_ \_ ADDRESS**   ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) プロパティにマップします。</span><span class="sxs-lookup"><span data-stu-id="bff5a-108">Finally, the method uses the [PropertyAccessor](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.recipient.propertyaccessor?redirectedfrom=MSDN&view=outlook-pia#Microsoft_Office_Interop_Outlook_Recipient_PropertyAccessor) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://docs.microsoft.com/office/client-developer/outlook/mapi/pidtagsmtpaddress-canonical-property?redirectedfrom=MSDN)) property of the recipient.</span></span>

<span data-ttu-id="bff5a-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bff5a-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bff5a-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bff5a-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bff5a-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bff5a-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    Outlook.Recipients recips = mail.Recipients;
    foreach (Outlook.Recipient recip in recips)
    {
        Outlook.PropertyAccessor pa = recip.PropertyAccessor;
        string smtpAddress =
            pa.GetProperty(PR_SMTP_ADDRESS).ToString();
        Debug.WriteLine(recip.Name + " SMTP=" + smtpAddress);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bff5a-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="bff5a-112">See also</span></span>

- [<span data-ttu-id="bff5a-113">受信者</span><span class="sxs-lookup"><span data-stu-id="bff5a-113">Recipients</span></span>](recipients.md)

