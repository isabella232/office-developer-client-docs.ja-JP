---
title: 複数のアカウントの情報を取得する
TOCTitle: Get information about multiple accounts
ms:assetid: 363f4058-3069-4ddc-b3ff-113a4dfd58c4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184599(v=office.15)
ms:contentKeyID: 55119794
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 42d0d8439473e9404cb2e94ed9e7e83d59b4c95c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406688"
---
# <a name="get-information-about-multiple-accounts"></a><span data-ttu-id="3eaae-102">複数のアカウントの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="3eaae-102">Get information about multiple accounts</span></span>

<span data-ttu-id="3eaae-p101">Outlook は、Exchange Server に接続される 1 つまたは複数のアカウントが入っているプロファイルをサポートしています。この例では、現在のプロファイル内の各アカウントの情報を取得して表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-p101">Outlook supports a profile that contains one or more accounts that are connected to an Exchange Server. This example shows how to obtain and display miscellaneous information about each account in the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="3eaae-105">例</span><span class="sxs-lookup"><span data-stu-id="3eaae-105">Example</span></span>

<span data-ttu-id="3eaae-p102">以下のメソッド EnumerateAccounts は、現在のプロファイルで定義されている各アカウントのアカウント名、ユーザー名、および SMTP (Simple Mail Transfer Protocol) アドレスを表示します。Exchange サーバーに接続されるアカウントについては、EnumerateAccounts は Exchange サーバーの名前とバージョン情報を表示します。また、配信ストア上にあるアカウントについては、EnumerateAccounts はそのアカウントの既定の配信ストアの名前を表示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-p102">The following method, EnumerateAccounts, displays the account name, user name, and Simple Mail Transfer Protocol (SMTP) address for each account that is defined in the current profile. If the account is connected to an Exchange server, EnumerateAccounts displays the Exchange server name and version information. And if the account resides on a delivery store, EnumerateAccounts displays the name of the default delivery store for the account.</span></span>

<span data-ttu-id="3eaae-109">EnumerateAccounts は、この情報の多くを [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトから取得します。ただし、**Account** オブジェクトにユーザー名と SMTP アドレスの情報が含まれていない場合を除きます。</span><span class="sxs-lookup"><span data-stu-id="3eaae-109">EnumerateAccounts accesses most of this information from the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object, except when the **Account** object does not contain information about the user name and SMTP address.</span></span> <span data-ttu-id="3eaae-110">その場合、EnumerateAccounts は [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトと [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを使用します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-110">In that case, EnumerateAccounts uses the [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) and [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) objects.</span></span> 

<span data-ttu-id="3eaae-111">EnumerateAccounts は [CurrentUser](https://msdn.microsoft.com/library/ff184864\(v=office.15\)) プロパティから取得した [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトの [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) メソッドを使用して、**AddressEntry** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-111"> obtains the AddressEntry object by using the AddressEntry property of the Recipient object obtained from the CurrentUser property.</span></span> <span data-ttu-id="3eaae-112">EnumerateAccounts は **AddressEntry** オブジェクトの [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドを使用して **ExchangeUser** オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-112"> obtains the ExchangeUser object by using the GetExchangeUser() method of the AddressEntry object.</span></span> 

<span data-ttu-id="3eaae-113">Account、AddressEntry、および ExchangeUser オブジェクトを使用して、各種の情報を取得するアルゴリズムを次に示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-113">The following is the algorithm to obtain various information by using the Account, AddressEntry, and ExchangeUser objects:</span></span>

- <span data-ttu-id="3eaae-114">**Account** オブジェクトにユーザー名と SMTP アドレスの情報が含まれている場合は、 **Account** オブジェクトを使用して、アカウント名、ユーザー名、SMTP アドレスを表示し、さらに Exchange のアカウントについては、Exchange サーバーの名前とバージョン情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-114">If the **Account** object contains information about the user name and SMTP address, use the **Account** object to display the account name, user name, SMTP address, and Exchange server name and version information if the account is an Exchange account.</span></span>

- <span data-ttu-id="3eaae-115">**Account** オブジェクトにユーザー名と SMTP アドレスの情報が含まれていない場合は、次のように処理します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-115">If the **Account** object does not contain information about the user name and SMTP address, proceed as follows:</span></span>
    
  - <span data-ttu-id="3eaae-116">アカウントが Exchange アカウントでないときは、 **AddressEntry** オブジェクトを使用してユーザー名と SMTP アドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-116">If the account is not an Exchange account, use the **AddressEntry** object to display the user name and SMTP address.</span></span>
    
  - <span data-ttu-id="3eaae-117">アカウントが Exchange アカウントのときは、次のように処理します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-117">If the account is an Exchange account, proceed as follows:</span></span>
        
    1.  <span data-ttu-id="3eaae-118">**Account** オブジェクトを使用して、アカウント名、Exchange サーバー名、および Exchange バージョン情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-118">Use the **Account** object to display the account name, Exchange server name, and Exchange version information.</span></span>
        
    2.  <span data-ttu-id="3eaae-119">**ExchangeUser** オブジェクトを使用して、ユーザー名と SMTP アドレスを表示します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-119">Use the **ExchangeUser** object to display the user name and SMTP address.</span></span>

<span data-ttu-id="3eaae-120">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3eaae-120">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="3eaae-121">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3eaae-121">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="3eaae-122">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3eaae-122">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3eaae-123">関連項目</span><span class="sxs-lookup"><span data-stu-id="3eaae-123">See also</span></span>

- [<span data-ttu-id="3eaae-124">アカウント</span><span class="sxs-lookup"><span data-stu-id="3eaae-124">Accounts</span></span>](accounts.md)

