---
title: 複数のアカウントの情報を取得する
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d065761b9296f1c0eb3043e9b9778e438790f94e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349414"
---
# <a name="get-information-about-multiple-accounts"></a>複数のアカウントの情報を取得する

Outlook は、Exchange Server に接続される 1 つまたは複数のアカウントが入っているプロファイルをサポートしています。この例では、現在のプロファイル内の各アカウントの情報を取得して表示する方法を示します。

## <a name="example"></a>例

以下のメソッド EnumerateAccounts は、現在のプロファイルで定義されている各アカウントのアカウント名、ユーザー名、および SMTP (Simple Mail Transfer Protocol) アドレスを表示します。Exchange サーバーに接続されるアカウントについては、EnumerateAccounts は Exchange サーバーの名前とバージョン情報を表示します。また、配信ストア上にあるアカウントについては、EnumerateAccounts はそのアカウントの既定の配信ストアの名前を表示します。

EnumerateAccounts は、この情報の多くを [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトから取得します。ただし、**Account** オブジェクトにユーザー名と SMTP アドレスの情報が含まれていない場合を除きます。 その場合、EnumerateAccounts は [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトと [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを使用します。 

EnumerateAccounts は [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)) プロパティから取得した [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトの [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) メソッドを使用して、**AddressEntry** オブジェクトを取得します。 EnumerateAccounts は **AddressEntry** オブジェクトの [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドを使用して **ExchangeUser** オブジェクトを取得します。 

Account、AddressEntry、および ExchangeUser オブジェクトを使用して、各種の情報を取得するアルゴリズムを次に示します。

- **Account** オブジェクトにユーザー名と SMTP アドレスの情報が含まれている場合は、 **Account** オブジェクトを使用して、アカウント名、ユーザー名、SMTP アドレスを表示し、さらに Exchange のアカウントについては、Exchange サーバーの名前とバージョン情報を表示します。

- **Account** オブジェクトにユーザー名と SMTP アドレスの情報が含まれていない場合は、次のように処理します。
    
  - アカウントが Exchange アカウントでないときは、 **AddressEntry** オブジェクトを使用してユーザー名と SMTP アドレスを表示します。
    
  - アカウントが Exchange アカウントのときは、次のように処理します。
        
    1.  **Account** オブジェクトを使用して、アカウント名、Exchange サーバー名、および Exchange バージョン情報を表示します。
        
    2.  **ExchangeUser** オブジェクトを使用して、ユーザー名と SMTP アドレスを表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAccounts()
{
    Outlook.Accounts accounts =
        Application.Session.Accounts;
    foreach (Outlook.Account account in accounts)
    {
        try
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Account: " + account.DisplayName);
            if (string.IsNullOrEmpty(account.SmtpAddress)
                || string.IsNullOrEmpty(account.UserName))
            {
                Outlook.AddressEntry oAE =
                    account.CurrentUser.AddressEntry
                    as Outlook.AddressEntry;
                if (oAE.Type == "EX")
                {
                    Outlook.ExchangeUser oEU =
                        oAE.GetExchangeUser()
                        as Outlook.ExchangeUser;
                    sb.AppendLine("UserName: " +
                        oEU.Name);
                    sb.AppendLine("SMTP: " +
                        oEU.PrimarySmtpAddress);
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
                else
                {
                    sb.AppendLine("UserName: " +
                        oAE.Name);
                    sb.AppendLine("SMTP: " +
                        oAE.Address);
                }
            }
            else
            {
                sb.AppendLine("UserName: " +
                    account.UserName);
                sb.AppendLine("SMTP: " +
                    account.SmtpAddress);
                if(account.AccountType == 
                    Outlook.OlAccountType.olExchange)
                {
                    sb.AppendLine("Exchange Server: " +
                        account.ExchangeMailboxServerName);
                    sb.AppendLine("Exchange Server Version: " +
                        account.ExchangeMailboxServerVersion); 
                }
            }
            if(account.DeliveryStore !=null)
            {
                sb.AppendLine("Delivery Store: " +
                    account.DeliveryStore.DisplayName);
            }
            sb.AppendLine("---------------------------------");
            Debug.Write(sb.ToString());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex.Message);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [アカウント](accounts.md)

