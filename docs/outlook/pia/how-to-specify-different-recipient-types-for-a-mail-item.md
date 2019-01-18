---
title: メール アイテムのさまざまな受信者の種類を指定する
TOCTitle: Specify different recipient types for a mail item
ms:assetid: 2a3ace9f-627c-4fdd-b182-afc1b53af85b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184598(v=office.15)
ms:contentKeyID: 55119871
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bf61a7fbb470291eae448a93c80866112c41407a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722530"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a>メール アイテムのさまざまな受信者の種類を指定する

この例では、メール アイテムの受信者の種類 (To、Cc、Bcc) をプログラムで設定する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード例では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの受信者が To、Cc、または Bcc 受信者かどうかを指定する方法を説明しています。 SetRecipientTypeForMail は **MailItem** オブジェクトを作成し、3 つの [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトを **MailItem** の [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションに追加して、各 **Recipient** オブジェクトの [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) プロパティに [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) 列挙の値を設定します。


> [!NOTE]
> **Recipient** オブジェクトの **Type** プロパティは int 型であり、特定の受信者の種類の列挙とは関連していません。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void SetRecipientTypeForMail()
{
    Outlook.MailItem mail = Application.CreateItem(
        Outlook.OlItemType.olMailItem) as Outlook.MailItem;
    mail.Subject = "Sample Message";
    Outlook.Recipient recipTo =
        mail.Recipients.Add("someone@example.com");
    recipTo.Type = (int)Outlook.OlMailRecipientType.olTo;
    Outlook.Recipient recipCc =
        mail.Recipients.Add("someonecc@example.com");
    recipCc.Type = (int)Outlook.OlMailRecipientType.olCC;
    Outlook.Recipient recipBcc =
        mail.Recipients.Add("someonebcc@example.com");
    recipBcc.Type = (int)Outlook.OlMailRecipientType.olBCC;
    mail.Recipients.ResolveAll();
    mail.Display(false);
}
```

## <a name="see-also"></a>関連項目

- [メール](mail.md)

