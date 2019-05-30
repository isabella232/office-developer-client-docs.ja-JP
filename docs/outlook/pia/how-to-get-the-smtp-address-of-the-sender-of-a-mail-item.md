---
title: メール アイテムの差出人の SMTP アドレスを取得する
TOCTitle: Get the SMTP address of the sender of a mail item
ms:assetid: 86e0c0aa-1696-4415-b25f-f9c1c29d88a9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184624(v=office.15)
ms:contentKeyID: 55119869
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: 05d52f24262f08a6326d464a2dc0d57d6d0510d7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542549"
---
# <a name="get-the-smtp-address-of-the-sender-of-a-mail-item"></a>メール アイテムの差出人の SMTP アドレスを取得する

この例では、メール アイテムの差出人の簡易メール転送プロトコル (SMTP) アドレスを取得します。

## <a name="example"></a>例

受信したメール アイテムの SMTP アドレスを確認するには、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [SenderEmailAddress](https://msdn.microsoft.com/library/bb622746\(v=office.15\)) プロパティを使用します。 ただし、組織の内部の送信者については、**SenderEmailAddress** によって SMTP アドレスは返されません。その送信者の SMTP アドレスを返す [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを使用する必要があります。

次のコード例では、GetSenderSMTPAddress で **PropertyAccessor** を使用することで、Outlook オブジェクト モデルでは直接公開されていない値を取得しています。 GetSenderSMTPAddress は、**MailItem** を受け取ります。 受信した [MailItem](https://msdn.microsoft.com/library/bb624136\(v=office.15\)) の **SenderEmailType** プロパティが "EX" の場合、そのメッセージの差出人は同じ組織内の Exchange サーバーに存在します。 GetSenderSMTPAddress では、**MailItem** オブジェクトの [Sender](https://msdn.microsoft.com/library/ff184720\(v=office.15\)) プロパティを使用して、[AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトで表される送信者を取得します。 その **AddressEntry** オブジェクトが Exchange ユーザーを表している場合、 [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドを使用して [AddressEntry](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトの **ExchangeUser** オブジェクトを取得します。 その後、GetSenderSMTPAddress では、**ExchangeUser** オブジェクトの [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) プロパティを使用して、送信者の SMTP アドレスを返します。 送信者の **AddressEntry** オブジェクトが **ExchangeUser** オブジェクトを表していない場合は、その送信者の SMTP アドレスを返すために、引数として **PR\_SMTP\_ADDRESS** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) を指定した **PropertyAccessor** オブジェクトの [GetProperty(String)](https://msdn.microsoft.com/library/bb645726\(v=office.15\)) メソッドを使用します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private string GetSenderSMTPAddress(Outlook.MailItem mail)
{
    string PR_SMTP_ADDRESS =
        @"http://schemas.microsoft.com/mapi/proptag/0x39FE001E";
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

## <a name="see-also"></a>関連項目

- [メール](mail.md)

