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
# <a name="send-an-email-given-the-smtp-address-of-an-account"></a>アカウントの SMTP アドレスを指定して電子メールを送信する

このトピックでは、電子メールを作成し、指定した簡易メール転送プロトコル (SMTP) アドレスを持つ Microsoft Outlook アカウントからその電子メールを送信する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、Helmut Obertanner 氏が提供したものです。 Helmut 氏の得意分野は、Office Developer Tools for Visual Studio と Outlook です。 


次のコード例には、Sample クラスの SendEmailFromAccount メソッドと GetAccountForEmailAddress メソッドが含まれています。これらは、Outlook アドイン プロジェクトの一部として実装されています。 それぞれのプロジェクトでは、[Microsoft.Office.Interop.Outlook](https://msdn.microsoft.com/library/bb610835\(v=office.15\)) 名前空間に基づいた、Outlook プライマリ互換運用機能アセンブリへの参照を追加しています。 SendEmailFromAccount メソッドは、信頼された [Application](https://msdn.microsoft.com/library/bb646615\(v=office.15\)) オブジェクト、件名、本文、受信者のセミコロン区切りリスト、および電子メール アカウントの SMTP アドレスを入力引数として受け取ります。 SendEmailFromAccount では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトを作成して、[To](https://msdn.microsoft.com/library/bb624372\(v=office.15\))、[Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\))、および [Body](https://msdn.microsoft.com/library/bb646600\(v=office.15\)) の各プロパティを指定された引数で初期化します。 電子メールの送信先から [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを見つけるために、SendEmailFromAccount で GetAccountForEmailAddress メソッドを呼び出します。このメソッドは、指定した SMTP アドレスと、現在のプロファイルに対応する各アカウントの [SmtpAddress](https://msdn.microsoft.com/library/bb623516\(v=office.15\)) プロパティを照合します。 SendEmailFromAccount に一致した **Account** オブジェクトが返され、この **Account** オブジェクトで **MailItem** の [SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) プロパティが初期化されて、**MailItem** が送信されます。

次に、Visual Basic のコード例を示します。その後に、C\# のコード例を示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [メール](mail.md)

