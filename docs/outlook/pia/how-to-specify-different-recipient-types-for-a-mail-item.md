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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335512"
---
# <a name="specify-different-recipient-types-for-a-mail-item"></a><span data-ttu-id="3e4e6-102">メール アイテムのさまざまな受信者の種類を指定する</span><span class="sxs-lookup"><span data-stu-id="3e4e6-102">Specify different recipient types for a mail item</span></span>

<span data-ttu-id="3e4e6-103">この例では、メール アイテムの受信者の種類 (To、Cc、Bcc) をプログラムで設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-103">This example shows how to programmatically set different recipient types (To, Cc, or Bcc) for a mail item.</span></span>

## <a name="example"></a><span data-ttu-id="3e4e6-104">例</span><span class="sxs-lookup"><span data-stu-id="3e4e6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3e4e6-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="3e4e6-106">次のコード例では、[MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) オブジェクトの受信者が To、Cc、または Bcc 受信者かどうかを指定する方法を説明しています。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-106">The following code example illustrates how to specify whether a recipient of a [MailItem](https://msdn.microsoft.com/library/bb643865\(v=office.15\)) object is a To, Cc, or Bcc recipient.</span></span> <span data-ttu-id="3e4e6-107">SetRecipientTypeForMail は **MailItem** オブジェクトを作成し、3 つの [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトを **MailItem** の [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) コレクションに追加して、各 **Recipient** オブジェクトの [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) プロパティに [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) 列挙の値を設定します。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-107">SetRecipientTypeForMail creates a **MailItem** object, adds three [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) objects to the [Recipients](https://msdn.microsoft.com/library/bb646361\(v=office.15\)) collection of the **MailItem**, and then sets the [Type](https://msdn.microsoft.com/library/bb611841\(v=office.15\)) property of each **Recipient** object to a value from the [OlMailRecipientType](https://msdn.microsoft.com/library/bb647641\(v=office.15\)) enumeration.</span></span>


> [!NOTE]
> <span data-ttu-id="3e4e6-108">**Recipient** オブジェクトの **Type** プロパティは int 型であり、特定の受信者の種類の列挙とは関連していません。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-108">The **Type** property of the **Recipient** object is an int type and does not correlate to a specific recipient type enumeration.</span></span>

<span data-ttu-id="3e4e6-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3e4e6-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3e4e6-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3e4e6-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="3e4e6-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="3e4e6-112">See also</span></span>

- [<span data-ttu-id="3e4e6-113">メール</span><span class="sxs-lookup"><span data-stu-id="3e4e6-113">Mail</span></span>](mail.md)

