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
# <a name="get-the-email-address-of-a-recipient"></a>受信者のメール アドレスを取得する

この例では、受信者の簡易メール転送プロトコル (SMTP) アドレスを取得する方法を示します。

## <a name="example"></a>例

次のコード例の GetSMTPAddressForRecipients メソッドは、入力引数として [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトを受け取り、そのメール アイテムの各受信者の SMTP アドレスを表示します。 このメソッドでは、最初にメール アイテムに対して指定されている一連の受信者を表す [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションを取得します。 その **Recipients** コレクションの [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) ごとに、その **Recipient** オブジェクトに対応する [PropertyAccessor](https://msdn.microsoft.com/library/bb646034\(v=office.15\)) オブジェクトを取得します。 MAPI プロパティの値を取得するメソッドが[PropertyAccessor](https://msdn.microsoft.com/library/bb623797\(v=office.15\))プロパティを使用して最後に、https://schemas.microsoft.com/mapi/proptag/0x39FE001Eに対応する、 **PR\_SMTP\_アドレス** ([PidTagSmtpAddress](https://msdn.microsoft.com/library/cc842421\(v=office.15\))) の受信者のプロパティです。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [受信者](recipients.md)

