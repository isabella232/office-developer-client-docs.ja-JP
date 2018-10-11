---
title: アカウントの SMTP アドレスを指定して電子メールを送信する
TOCTitle: Send an email given the SMTP address of an account
ms:assetid: 4ff4aaac-54ba-45c7-8b2e-aeba35af1e56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff462095(v=office.15)
ms:contentKeyID: 55119865
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 01eef87c70e27425182b8a2f9f849c9736d43a31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406394"
---
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a><span data-ttu-id="b60f7-102">アカウントの SMTP アドレスを指定して電子メールを送信する</span><span class="sxs-lookup"><span data-stu-id="b60f7-102">Send an E-mail Given the SMTP Address of an Account</span></span>

<span data-ttu-id="b60f7-103">このトピックでは、電子メールを作成し、指定した簡易メール転送プロトコル (SMTP) アドレスを持つ Microsoft Outlook アカウントからその電子メールを送信する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="b60f7-103">This topic shows how to create an e-mail and send it from a Microsoft Outlook account, given the Simple Mail Transfer Protocol (SMTP) address of that account.</span></span>

## <a name="example"></a><span data-ttu-id="b60f7-104">例</span><span class="sxs-lookup"><span data-stu-id="b60f7-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="b60f7-105">次のコード例は、Helmut Obertanner 氏が提供したものです。</span><span class="sxs-lookup"><span data-stu-id="b60f7-105">Helmut Obertanner provided the following code examples.</span></span> <span data-ttu-id="b60f7-106">Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。</span><span class="sxs-lookup"><span data-stu-id="b60f7-106">Helmut Obertanner provided the following code examples. Helmut's expertise is in Office Developer Tools for Visual Studio and Outlook. Helmut maintains a professional site at X4Uelectronix.</span></span> 


<span data-ttu-id="b60f7-107">次のコード例には、Sample クラスの SendEmailFromAccount メソッドと GetAccountForEmailAddress メソッドが含まれています。これらは、Outlook アドイン プロジェクトの一部として実装されています。</span><span class="sxs-lookup"><span data-stu-id="b60f7-107">The following code examples contain the   method of the   class, implemented as part of an Outlook add-in project.</span></span> <span data-ttu-id="b60f7-108">それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。</span><span class="sxs-lookup"><span data-stu-id="b60f7-108">Each project adds a reference to the Outlook Primary Interop Assembly, which is based on the [Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) namespace.</span></span> <span data-ttu-id="b60f7-109">SendEmailFromAccount メソッドは、信頼された [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクト、件名、本文、受信者のセミコロン区切りリスト、および電子メール アカウントの SMTP アドレスを入力引数として受け取ります。</span><span class="sxs-lookup"><span data-stu-id="b60f7-109">The SendEmailFromAccount method accepts as input arguments a trusted [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) object, and strings that represent the subject, body, a semicolon-delimited list of recipients, and the SMTP address of an email account.</span></span> <span data-ttu-id="b60f7-110">SendEmailFromAccount では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトを作成して、[To](https://msdn.microsoft.com/library/bb624372\(v=office.15\))、[Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\))、および [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) の各プロパティを指定された引数で初期化します。</span><span class="sxs-lookup"><span data-stu-id="b60f7-110">SendEmailFromAccount creates a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object and initializes the [To](https://msdn.microsoft.com/library/bb624372\(v=office.15\)), [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)), and [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) properties with the given arguments.</span></span> <span data-ttu-id="b60f7-111">電子メールの送信先から [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを見つけるために、SendEmailFromAccount で GetAccountForEmailAddress メソッドを呼び出します。このメソッドは、指定した SMTP アドレスと、現在のプロファイルに対応する各アカウントの [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) プロパティを照合します。</span><span class="sxs-lookup"><span data-stu-id="b60f7-111">To find the [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) object from which to send the email, SendEmailFromAccount calls the GetAccountForEmailAddress method, which matches the given SMTP address with the [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) property of each account for the current profile.</span></span> <span data-ttu-id="b60f7-112">SendEmailFromAccount に一致した **Account** オブジェクトが返され、この **Account** オブジェクトで **MailItem** の [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) プロパティが初期化されて、**MailItem** が送信されます。</span><span class="sxs-lookup"><span data-stu-id="b60f7-112">The matching **Account** object is returned to SendEmailFromAccount, which then initializes the [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) property of the **MailItem** with this **Account** object, and sends the **MailItem**.</span></span>

<span data-ttu-id="b60f7-113">次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。</span><span class="sxs-lookup"><span data-stu-id="b60f7-113">The following is the Visual Basic code example, followed by the C# code example.</span></span>

<span data-ttu-id="b60f7-114">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b60f7-114">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="b60f7-115">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b60f7-115">The Imports or using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="b60f7-116">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="b60f7-116">The following lines of code show how to do the import and assignment in Visual Basic and C#.</span></span>

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Imports Outlook = Microsoft.Office.Interop.Outlook

Namespace OutlookAddIn2
    Class Sample
        
        Shared Sub SendEmailFromAccount(ByVal application As Outlook.Application, _
            ByVal subject As String, ByVal body As String, ByVal recipients As String, ByVal smtpAddress As String)

            ' Create a new MailItem and set the To, Subject, and Body properties.
            Dim newMail As Outlook.MailItem = DirectCast(application.CreateItem(Outlook.OlItemType.olMailItem), Outlook.MailItem)
            newMail.To = recipients
            newMail.Subject = subject
            newMail.Body = body

            ' Retrieve the account that has the specific SMTP address.
            Dim account As Outlook.Account = GetAccountForEmailAddress(application, smtpAddress)
            ' Use this account to send the email.
            newMail.SendUsingAccount = account
            newMail.Send()
        End Sub

        Shared Function GetAccountForEmailAddress(ByVal application As Outlook.Application, ByVal smtpAddress As String) As Outlook.Account

            ' Loop over the Accounts collection of the current Outlook session.
            Dim accounts As Outlook.Accounts = application.Session.Accounts
            Dim account As Outlook.Account
            For Each account In accounts
                ' When the email address matches, return the account.
                If account.SmtpAddress = smtpAddress Then
                    Return account
                End If
            Next
            Throw New System.Exception(String.Format("No Account with SmtpAddress: {0} exists!", smtpAddress))
        End Function

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
        public static void SendEmailFromAccount(Outlook.Application application, string subject, string body, string to, string smtpAddress)
        {

            // Create a new MailItem and set the To, Subject, and Body properties.
            Outlook.MailItem newMail = (Outlook.MailItem)application.CreateItem(Outlook.OlItemType.olMailItem);
            newMail.To = to;
            newMail.Subject = subject;
            newMail.Body = body;

            // Retrieve the account that has the specific SMTP address.
            Outlook.Account account = GetAccountForEmailAddress(application, smtpAddress);
            // Use this account to send the email.
            newMail.SendUsingAccount = account;
            newMail.Send();
        }


        public static Outlook.Account GetAccountForEmailAddress(Outlook.Application application, string smtpAddress)
        {

            // Loop over the Accounts collection of the current Outlook session.
            Outlook.Accounts accounts = application.Session.Accounts;
            foreach (Outlook.Account account in accounts)
            {
                // When the email address matches, return the account.
                if (account.SmtpAddress == smtpAddress)
                {
                    return account;
                }
            }
            throw new System.Exception(string.Format("No Account with SmtpAddress: {0} exists!", smtpAddress));
        }

    }
}
```

## <a name="see-also"></a><span data-ttu-id="b60f7-117">関連項目</span><span class="sxs-lookup"><span data-stu-id="b60f7-117">See also</span></span>

- [<span data-ttu-id="b60f7-118">メール</span><span class="sxs-lookup"><span data-stu-id="b60f7-118">Mail</span></span>](mail.md)

