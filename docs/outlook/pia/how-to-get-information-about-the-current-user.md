---
title: 現在のユーザーの情報を取得する
TOCTitle: Get information about the current user
ms:assetid: 3802523a-3ccf-4cca-a348-abe2645a0d9c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184601(v=office.15)
ms:contentKeyID: 55119840
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 7ac10c01d205f4f4590183bcef8006e8f1344cbd
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406975"
---
# <a name="get-information-about-the-current-user"></a><span data-ttu-id="0ef49-102">現在のユーザーの情報を取得する</span><span class="sxs-lookup"><span data-stu-id="0ef49-102">Get information about the current user</span></span>

<span data-ttu-id="0ef49-103">この例では、現在のユーザーの情報 (名前、役職、電話番号など) を取得する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0ef49-103">This example shows how to get the current user’s information, such as name, job title, and telephone number.</span></span>

## <a name="example"></a><span data-ttu-id="0ef49-104">例</span><span class="sxs-lookup"><span data-stu-id="0ef49-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="0ef49-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="0ef49-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="0ef49-106">[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトから取得するには、**AddressEntry** オブジェクトの [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="0ef49-106">To obtain an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object from an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object, call the [GetExchangeUser()](https://msdn.microsoft.com/library/bb611808\(v=office.15\)) method on the **AddressEntry** object.</span></span> <span data-ttu-id="0ef49-107">次のプロシージャで GetCurrentUserInfo は、[CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) プロパティを使用して、[Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトの [AddressEntry](https://msdn.microsoft.com/library/bb644359\(v=office.15\)) プロパティを取得します。</span><span class="sxs-lookup"><span data-stu-id="0ef49-107">In the following procedure,   gets the AddressEntry property for the Recipient object by using the CurrentUser property.</span></span> <span data-ttu-id="0ef49-108">**AddressEntry** オブジェクトが Exchange メールボックス ユーザーを表している場合、GetCurrentUserInfo は **GetExchangeUser** メソッドを呼び出し、**ExchangeUser** オブジェクトが返されます。</span><span class="sxs-lookup"><span data-stu-id="0ef49-108">If the AddressEntry object represents an Exchange mailbox user,   calls the GetExchangeUser method and an ExchangeUser object is returned.</span></span> <span data-ttu-id="0ef49-109">[Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\))、[PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\))、[JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\))、[Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\))、[OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\))、[BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\))、および [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) の各プロパティが、[Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き出されます。</span><span class="sxs-lookup"><span data-stu-id="0ef49-109">The [Name](https://msdn.microsoft.com/library/bb622941\(v=office.15\)) , [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) , [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)) , [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)) , [OfficeLocation](https://msdn.microsoft.com/library/bb611429\(v=office.15\)) , [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)) , and [MobileTelephoneNumber](https://msdn.microsoft.com/library/bb609292\(v=office.15\)) properties are written to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="0ef49-110">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0ef49-110">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="0ef49-111">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0ef49-111">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="0ef49-112">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="0ef49-112">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserInfo()
{
    Outlook.AddressEntry addrEntry =
        Application.Session.CurrentUser.AddressEntry;
    if (addrEntry.Type == "EX")
    {
        Outlook.ExchangeUser currentUser =
            Application.Session.CurrentUser.
            AddressEntry.GetExchangeUser();
        if (currentUser != null)
        {
            StringBuilder sb = new StringBuilder();
            sb.AppendLine("Name: "
                + currentUser.Name);
            sb.AppendLine("STMP address: "
                + currentUser.PrimarySmtpAddress);
            sb.AppendLine("Title: "
                + currentUser.JobTitle);
            sb.AppendLine("Department: "
                + currentUser.Department);
            sb.AppendLine("Location: "
                + currentUser.OfficeLocation);
            sb.AppendLine("Business phone: "
                + currentUser.BusinessTelephoneNumber);
            sb.AppendLine("Mobile phone: "
                + currentUser.MobileTelephoneNumber);
            Debug.WriteLine(sb.ToString());
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="0ef49-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="0ef49-113">See also</span></span>

- [<span data-ttu-id="0ef49-114">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="0ef49-114">Exchange Users</span></span>](exchange-users.md)

