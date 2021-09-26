---
title: Hotmail アカウントを使用してメール アイテムを送信する
TOCTitle: Send a mail item by using a Hotmail account
ms:assetid: f25853a7-67c0-46a3-a298-5cdf72ebc53f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184652(v=office.15)
ms:contentKeyID: 55119797
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2771e867cc4e20f35c2d449a62ff6f2acee3b2e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629264"
---
# <a name="send-a-mail-item-by-using-a-hotmail-account"></a>Hotmail アカウントを使用してメール アイテムを送信する

この例では、Windows Live Hotmail アカウントを使用してメール アイテムを送信するために、[SendUsingAccount](https://msdn.microsoft.com/library/bb623679\(v=office.15\)) プロパティを使用しています。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

プロファイルでは、1 つ以上の電子メール アカウントを定義します。それぞれの電子メール アカウントは特定の種類 (Microsoft Exchange Server や Post Office Protocol 3 (POP3) など) に関連付けられています。 プロファイルには複数のアカウントが含まれていることがあるため、アイテムの送信に使用する電子メール アカウントを指定してから、そのアカウントを表す [Account](https://msdn.microsoft.com/library/bb645103\(v=office.15\)) オブジェクトを取得する必要があります。

次のコード例では、旅程表が添付されたメッセージを作成してから、Windows Live Hotmail アカウントを使用して送信します。 この Hotmail 電子メール アカウントは、ユーザーのプロファイルに含まれる **Account** オブジェクトとして使用されます。 その後、SendUsingAccount プロパティをそのアカウントに設定して、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの [Send()](https://msdn.microsoft.com/library/bb644139\(v=office.15\)) メソッドを呼び出します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void SendUsingAccountExample()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Our itinerary";
    mail.Attachments.Add(@"c:\travel\itinerary.doc",
        Outlook.OlAttachmentType.olByValue,
        Type.Missing, Type.Missing);
    Outlook.Account account =
        Application.Session.Accounts["Hotmail"];
    mail.SendUsingAccount = account;
    mail.Send();
}
```

## <a name="see-also"></a>関連項目

- [アカウント](accounts.md)

