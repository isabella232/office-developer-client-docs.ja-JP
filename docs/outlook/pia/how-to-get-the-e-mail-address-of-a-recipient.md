---
title: 受信者のメール アドレスを取得する
TOCTitle: Get the email address of a recipient
ms:assetid: e585811b-a298-496f-ba79-df7d46526169
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184647(v=office.15)
ms:contentKeyID: 55119879
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 030908f7202301ec7849e655d5ff7cc1d7cffc13
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719331"
---
# <a name="get-the-email-address-of-a-recipient"></a><span data-ttu-id="3be67-102">受信者のメール アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="3be67-102">Get the email address of a recipient</span></span>

<span data-ttu-id="3be67-103">この例では、受信者の簡易メール転送プロトコル (SMTP) アドレスを取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3be67-103">This example shows how to get the Simple Mail Transfer Protocol (SMTP) address of a recipient.</span></span>

## <a name="example"></a><span data-ttu-id="3be67-104">例</span><span class="sxs-lookup"><span data-stu-id="3be67-104">Example</span></span>

<span data-ttu-id="3be67-105">次のコード例の GetSMTPAddressForRecipients メソッドは、入力引数として [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトを受け取り、そのメール アイテムの各受信者の SMTP アドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="3be67-105">In the following the code example, the GetSMTPAddressForRecipients method takes a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object as an input argument and then displays the SMTP address of each recipient for that mail item.</span></span> <span data-ttu-id="3be67-106">このメソッドでは、最初にメール アイテムに対して指定されている一連の受信者を表す [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="3be67-106">The method first retrieves the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection that represents the set of recipients specified for the mail item.</span></span> <span data-ttu-id="3be67-107">その **Recipients** コレクションの [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) ごとに、その **Recipient** オブジェクトに対応する [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3be67-107">For each [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) in that **Recipients** collection, the method then obtains the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object that corresponds to that **Recipient** object.</span></span> <span data-ttu-id="3be67-108">MAPI プロパティの値を取得するメソッドが[PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\))プロパティを使用して最後に、https://schemas.microsoft.com/mapi/proptag/0x39FE001Eに対応する、 **PR\_SMTP\_アドレス** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) の受信者のプロパティです。</span><span class="sxs-lookup"><span data-stu-id="3be67-108">Finally, the method uses the [PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\)) property to get the value of the MAPI property https://schemas.microsoft.com/mapi/proptag/0x39FE001E, which maps to the **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) property of the recipient.</span></span>

<span data-ttu-id="3be67-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3be67-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3be67-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3be67-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3be67-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3be67-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetSMTPAddressForRecipients(Outlook.MailItem mail)
{
    const string PR_SMTP_ADDRESS =
        "https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a><span data-ttu-id="3be67-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="3be67-112">See also</span></span>

- [<span data-ttu-id="3be67-113">受信者</span><span class="sxs-lookup"><span data-stu-id="3be67-113">Recipients</span></span>](recipients.md)

