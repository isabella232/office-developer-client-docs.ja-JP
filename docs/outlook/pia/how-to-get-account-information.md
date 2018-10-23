---
title: アカウント情報を取得する
TOCTitle: Get account information
ms:assetid: 02825449-50eb-42d0-8e45-361db5f473df
ms:contentKeyID: 55119795
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 8af09a6cab56dc80015ecd507a9a2adf423c1978
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406170"
---
# <a name="get-account-information"></a><span data-ttu-id="64287-102">アカウント情報を取得する</span><span class="sxs-lookup"><span data-stu-id="64287-102">Get account information</span></span>

<span data-ttu-id="64287-103">このトピックでは、信頼される Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクトを入力引数として受け取り、 **Account** オブジェクトを使用して、現在の Outlook プロファイル用に使用できる各アカウントの詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="64287-103">This topic takes as an input argument a trusted Outlook [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object, and uses the **Account** object to display the details of each account that is available for the current Outlook profile.</span></span>

## <a name="example"></a><span data-ttu-id="64287-104">例</span><span class="sxs-lookup"><span data-stu-id="64287-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="64287-105">次のコード例は、Helmut Obertanner 氏が提供したものです。</span><span class="sxs-lookup"><span data-stu-id="64287-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="64287-106">Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。</span><span class="sxs-lookup"><span data-stu-id="64287-106">Helmut Obertanner provided the following code examples. Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook. Helmut maintains a professional site at X4Uelectronix.</span></span> 

<span data-ttu-id="64287-107">次のコード例には、Sample クラスの DisplayAccountInformation メソッドが含まれています。このメソッドは、Outlook アドイン プロジェクトの一部として実装されています。</span><span class="sxs-lookup"><span data-stu-id="64287-107">The following code examples contain the   method of the   class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="64287-108">それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。</span><span class="sxs-lookup"><span data-stu-id="64287-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span>

<span data-ttu-id="64287-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="64287-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="64287-110">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64287-110">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="64287-111">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="64287-111">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

<span data-ttu-id="64287-112">次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="64287-112">The following is the Visual Basic code example, followed by the C# code example.</span></span>


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        Shared Sub DisplayAccountInformation(ByVal application As Outlook.Application)

            ' The Namespace Object (Session) has a collection of accounts.
            Dim accounts As Outlook.Accounts = application.Session.Accounts

            ' Concatenate a message with information about all accounts.
            Dim builder As StringBuilder = New StringBuilder()

            ' Loop over all accounts and print detail account information.
            ' All properties of the Account object are read-only.
            Dim account As Outlook.Account
            For Each account In accounts

                ' The DisplayName property represents the friendly name of the account.
                builder.AppendFormat("DisplayName: {0}" & vbNewLine, account.DisplayName)

                ' The UserName property provides an account-based context to determine identity.
                builder.AppendFormat("UserName: {0}" & vbNewLine, account.UserName)

                ' The SmtpAddress property provides the SMTP address for the account.
                builder.AppendFormat("SmtpAddress: {0}" & vbNewLine, account.SmtpAddress)

                ' The AccountType property indicates the type of the account.
                builder.Append("AccountType: ")
                Select Case (account.AccountType)

                    Case Outlook.OlAccountType.olExchange
                        builder.AppendLine("Exchange")


                    Case Outlook.OlAccountType.olHttp
                        builder.AppendLine("Http")


                    Case Outlook.OlAccountType.olImap
                        builder.AppendLine("Imap")


                    Case Outlook.OlAccountType.olOtherAccount
                        builder.AppendLine("Other")


                    Case Outlook.OlAccountType.olPop3
                        builder.AppendLine("Pop3")


                End Select

                builder.AppendLine()
            Next


            ' Display the account information.
            Windows.Forms.MessageBox.Show(builder.ToString())
        End Sub


    End Class
End Namespace
```



```csharp
using System;
using System.Text;
using Outlook = Microsoft.Office.Interop.Outlook;

namespace OutlookAddIn1
{
    class Sample
    {
        public static void DisplayAccountInformation(Outlook.Application application)
        {

            // The Namespace Object (Session) has a collection of accounts.
            Outlook.Accounts accounts = application.Session.Accounts;

            // Concatenate a message with information about all accounts.
            StringBuilder builder = new StringBuilder();

            // Loop over all accounts and print detail account information.
            // All properties of the Account object are read-only.
            foreach (Outlook.Account account in accounts)
            {

                // The DisplayName property represents the friendly name of the account.
                builder.AppendFormat("DisplayName: {0}\n", account.DisplayName);

                // The UserName property provides an account-based context to determine identity.
                builder.AppendFormat("UserName: {0}\n", account.UserName);

                // The SmtpAddress property provides the SMTP address for the account.
                builder.AppendFormat("SmtpAddress: {0}\n", account.SmtpAddress);

                // The AccountType property indicates the type of the account.
                builder.Append("AccountType: ");
                switch (account.AccountType)
                {

                    case Outlook.OlAccountType.olExchange:
                        builder.AppendLine("Exchange");
                        break;

                    case Outlook.OlAccountType.olHttp:
                        builder.AppendLine("Http");
                        break;

                    case Outlook.OlAccountType.olImap:
                        builder.AppendLine("Imap");
                        break;

                    case Outlook.OlAccountType.olOtherAccount:
                        builder.AppendLine("Other");
                        break;

                    case Outlook.OlAccountType.olPop3:
                        builder.AppendLine("Pop3");
                        break;
                }

                builder.AppendLine();
            }

            // Display the account information.
            System.Windows.Forms.MessageBox.Show(builder.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="64287-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="64287-113">See also</span></span>

- [<span data-ttu-id="64287-114">アカウント</span><span class="sxs-lookup"><span data-stu-id="64287-114">Accounts</span></span>](accounts.md)
