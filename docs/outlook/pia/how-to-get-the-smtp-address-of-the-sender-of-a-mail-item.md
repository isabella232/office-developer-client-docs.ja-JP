---
title: メール アイテムの差出人の SMTP アドレスを取得する
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 74adbf02180e0e993b22e35481f51d304b14e7d6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320084"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a><span data-ttu-id="cf6a7-102">メール アイテムの差出人の SMTP アドレスを取得する</span><span class="sxs-lookup"><span data-stu-id="cf6a7-102">Get the SMTP address of the sender of a mail item</span></span>

<span data-ttu-id="cf6a7-103">この例では、メール アイテムの差出人の簡易メール転送プロトコル (SMTP) アドレスを取得します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-103">This example gets the sender’s Simple Mail Transfer Protocol (SMTP) address for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="cf6a7-104">例</span><span class="sxs-lookup"><span data-stu-id="cf6a7-104">Example</span></span>

<span data-ttu-id="cf6a7-105">受信したメール アイテムの SMTP アドレスを確認するには、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-105">To determine the SMTP address for a received mail item, use the [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) property of the [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object.</span></span> <span data-ttu-id="cf6a7-106">ただし、組織の内部の送信者については、**SenderEmailAddress** によって SMTP アドレスは返されません。その送信者の SMTP アドレスを返す [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-106">However, if the sender is internal to your organization, **SenderEmailAddress** does not return an SMTP address, and you must use the [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) object to return the sender’s SMTP address.</span></span>

<span data-ttu-id="cf6a7-107">次のコード例では、GetSenderSMTPAddress で **PropertyAccessor** を使用することで、Outlook オブジェクト モデルでは直接公開されていない値を取得しています。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-107">In the following code example, GetSenderSMTPAddress uses the **PropertyAccessor** object to obtain values that are not exposed directly in the Outlook object model.</span></span> <span data-ttu-id="cf6a7-108">GetSenderSMTPAddress は、**MailItem** を受け取ります。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-108">GetSenderSMTPAddress takes in a **MailItem**.</span></span> <span data-ttu-id="cf6a7-109">受信した [MailItem](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) の **SenderEmailType** プロパティが "EX" の場合、そのメッセージの差出人は同じ組織内の Exchange サーバーに存在します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-109">If the value of the [SenderEmailType](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) property of the received **MailItem** is "EX", the sender of the message resides on an Exchange server in your organization.</span></span> <span data-ttu-id="cf6a7-110">GetSenderSMTPAddress では、**MailItem** オブジェクトの [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) プロパティを使用して、[AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトで表される送信者を取得します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-110">GetSenderSMTPAddress uses the [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) property of the **MailItem** object to get the sender, represented by the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object.</span></span> <span data-ttu-id="cf6a7-111">その **AddressEntry** オブジェクトが Exchange ユーザーを表している場合、 [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドを使用して [AddressEntry](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトの **ExchangeUser** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-111">If the **AddressEntry** object represents an Exchange user, the example calls the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method to return the [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object of the **AddressEntry** object.</span></span> <span data-ttu-id="cf6a7-112">その後、GetSenderSMTPAddress では、**ExchangeUser** オブジェクトの [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) プロパティを使用して、送信者の SMTP アドレスを返します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-112">GetSenderSMTPAddress then uses the [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) property of the **ExchangeUser** object to return the SMTP address of the sender.</span></span> <span data-ttu-id="cf6a7-113">送信者の **AddressEntry** オブジェクトが **ExchangeUser** オブジェクトを表していない場合は、その送信者の SMTP アドレスを返すために、引数として **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) を指定した **PropertyAccessor** オブジェクトの [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-113">If the **AddressEntry** object for the sender does not represent an **ExchangeUser** object, the [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) method of the **PropertyAccessor** object is used, with **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) as the argument, to return the sender’s SMTP address.</span></span>

<span data-ttu-id="cf6a7-114">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="cf6a7-115">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-115">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="cf6a7-116">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="cf6a7-116">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"https://schemas.microsoft.com/mapi/proptag/0x39FE001E";
    if (mail == null)
    {
        throw new ArgumentNullException();
    }
    if (mail.SenderEmailType == "EX")
    {
        Outlook.AddressEntry sender =
            mail.Sender;
        if (sender != null)
        {
            //Now we have an AddressEntry representing the Sender
            if (sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || sender.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                //Use the ExchangeUser object PrimarySMTPAddress
                Outlook.ExchangeUser exchUser =
                    sender.GetExchangeUser();
                if (exchUser != null)
                {
                    return exchUser.PrimarySmtpAddress;
                }
                else
                {
                    return null;
                }
            }
            else
            {
                return sender.PropertyAccessor.GetProperty(
                    PR_SMTP_ADDRESS) as string;
            }
        }
        else
        {
            return null;
        }
    }
    else
    {
        return mail.SenderEmailAddress;
    }
}
```

## <a name="see-also"></a><span data-ttu-id="cf6a7-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="cf6a7-117">See also</span></span>

- [<span data-ttu-id="cf6a7-118">メール</span><span class="sxs-lookup"><span data-stu-id="cf6a7-118">Mail</span></span>](mail.md)

