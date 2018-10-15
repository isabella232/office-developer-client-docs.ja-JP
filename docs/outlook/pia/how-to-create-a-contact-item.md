---
title: 連絡先アイテムを作成する
TOCTitle: Create a Contact item
ms:assetid: b316294a-7f70-4e54-9375-4dc515e9fd11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184633(v=office.15)
ms:contentKeyID: 55119823
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 814885b209020fb37c84df2e88f04bb32ec5cd6c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407129"
---
# <a name="create-a-contact-item"></a><span data-ttu-id="e9f6a-102">連絡先アイテムを作成する</span><span class="sxs-lookup"><span data-stu-id="e9f6a-102">Create a Contact item</span></span>

<span data-ttu-id="e9f6a-103">この例では、連絡先アイテムを作成し、連絡先のさまざまなプロパティを設定する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-103">This example shows how to create a contact item and set various properties for the contact.</span></span>

## <a name="example"></a><span data-ttu-id="e9f6a-104">例</span><span class="sxs-lookup"><span data-stu-id="e9f6a-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="e9f6a-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="e9f6a-106">Outlook [ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) オブジェクトは、[Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\))、[CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\))、[OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\))、および [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) など、100 個以上の組み込みプロパティを持っています。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-106">An Outlook[ContactItem](https://msdn.microsoft.com/library/bb644956\(v=office.15\)) object has more than 100 built-in properties such as [Department](https://msdn.microsoft.com/library/bb610564\(v=office.15\)) , [CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\)) , [OfficeLocation](https://msdn.microsoft.com/library/bb647145\(v=office.15\)) , and [JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) .</span></span> <span data-ttu-id="e9f6a-107">これらの組み込みプロパティが使用できない場合は、[UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) コレクションを使用してカスタム プロパティを追加できます。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-107">You can add custom properties, if a built-in property is not available, by using the [UserProperties](https://msdn.microsoft.com/library/bb611428\(v=office.15\)) collection.</span></span> <span data-ttu-id="e9f6a-108">**ContactItem** を作成すると、カスタム プロパティを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-108">Once you create a **ContactItem**, you can set its properties.</span></span>

<span data-ttu-id="e9f6a-109">次のコード例の CreateContactExample は **ContactItem** を作成し、そのオブジェクトで共通に使用されるプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-109">In the following code example,   creates a ContactItem and sets commonly used properties for that object.</span></span> <span data-ttu-id="e9f6a-110">次に、**ContactItem** オブジェクトの [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-110">It then calls the [ShowCheckPhoneDialog(OlContactPhoneNumber)](https://msdn.microsoft.com/library/bb646168\(v=office.15\)) method on the **ContactItem** object.</span></span> <span data-ttu-id="e9f6a-111">**ShowCheckPhoneDialog** メソッドを使用すると、ユーザーはローカルのダイヤル方式に基づいて、電話番号を解決できます。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-111">The **ShowCheckPhoneDialog** method allows the user to resolve a phone number based on local dialing conventions.</span></span>

<span data-ttu-id="e9f6a-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="e9f6a-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="e9f6a-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="e9f6a-114">The following line of code shows how to do the import and assignment in C#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="e9f6a-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="e9f6a-115">See also</span></span>

- [<span data-ttu-id="e9f6a-116">連絡先</span><span class="sxs-lookup"><span data-stu-id="e9f6a-116">Contacts</span></span>](contacts.md)

