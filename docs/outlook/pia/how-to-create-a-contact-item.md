---
title: 連絡先アイテムを作成する
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 11bfe40d29832577186712e269f9c0971e1e2be6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359676"
---
# <a name="create-a-contact-item"></a>連絡先アイテムを作成する

この例では、連絡先アイテムを作成し、連絡先のさまざまなプロパティを設定する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) オブジェクトは、[Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\))、[CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\))、[OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\))、および [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) など、100 個以上の組み込みプロパティを持っています。 これらの組み込みプロパティが使用できない場合は、[UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) コレクションを使用してカスタム プロパティを追加できます。 **ContactItem** を作成すると、カスタム プロパティを設定できます。

次のコード例の CreateContactExample は **ContactItem** を作成し、そのオブジェクトで共通に使用されるプロパティを設定します。 次に、**ContactItem** オブジェクトの [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) メソッドを呼び出します。 **ShowCheckPhoneDialog** メソッドを使用すると、ユーザーはローカルのダイヤル方式に基づいて、電話番号を解決できます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateContactExample()
{
    Outlook.ContactItem contact = Application.CreateItem(
        Outlook.OlItemType.olContactItem) as Outlook.ContactItem;
    contact.FirstName = "Mellissa";
    contact.LastName = "MacBeth";
    contact.JobTitle = "Account Representative";
    contact.CompanyName = "Contoso Ltd.";
    contact.OfficeLocation = "36/2529";
    contact.BusinessTelephoneNumber = "4255551212 x432";
    contact.WebPage = "https://www.contoso.com";
    contact.BusinessAddressStreet = "1 Microsoft Way";
    contact.BusinessAddressCity = "Redmond";
    contact.BusinessAddressState = "WA";
    contact.BusinessAddressPostalCode = "98052";
    contact.BusinessAddressCountry =
        "United States of America";
    contact.Email1Address = "melissa@contoso.com";
    contact.Email1AddressType = "SMTP";
    contact.Email1DisplayName =
        "Melissa MacBeth (mellissa@contoso.com)";
    contact.Display(false);
    contact.ShowCheckPhoneDialog(
        Outlook.OlContactPhoneNumber.
        olContactPhoneBusiness);
}
```

## <a name="see-also"></a>関連項目

- [連絡先](contacts.md)

