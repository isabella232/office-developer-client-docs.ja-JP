---
title: グローバル アドレス一覧のエントリを列挙する
TOCTitle: Enumerate the entries in the Global Address List
ms:assetid: f3dfe312-fe91-475d-8435-1c7a0bb2b725
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184654(v=office.15)
ms:contentKeyID: 55119801
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 98256ce539172b69c2ae94d495c4aab12e3b8cc4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320364"
---
# <a name="enumerate-the-entries-in-the-global-address-list"></a><span data-ttu-id="fc27c-102">グローバル アドレス一覧のエントリを列挙する</span><span class="sxs-lookup"><span data-stu-id="fc27c-102">Enumerate the entries in the Global Address List</span></span>

<span data-ttu-id="fc27c-103">この例では、グローバル アドレス一覧 (GAL) に含まれる簡易メール転送プロトコル (SMTP) のプライマリ アドレスから最初の 100 件を列挙します。</span><span class="sxs-lookup"><span data-stu-id="fc27c-103">This example enumerates the first 100 primary Simple Mail Transfer Protocol (SMTP) addresses in the Global Address List (GAL).</span></span>

## <a name="example"></a><span data-ttu-id="fc27c-104">例</span><span class="sxs-lookup"><span data-stu-id="fc27c-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="fc27c-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="fc27c-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="fc27c-106">次のコード例では、[AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) オブジェクトの SMTP アドレスを、 [GetExchangeUser()](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) メソッドまたは [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) メソッドの呼び出しで [ExchangeUser](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) オブジェクトまたは [ExchangeDistributionList](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) オブジェクトにキャストすることで取得します。</span><span class="sxs-lookup"><span data-stu-id="fc27c-106">In the following code example, the SMTP address for an [AddressEntry](https://msdn.microsoft.com/library/bb609728\(v=office.15\)) object is obtained by casting it to an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) or [ExchangeDistributionList](https://msdn.microsoft.com/library/bb624320\(v=office.15\)) object in a call to the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) or [GetExchangeDistributionList()](https://msdn.microsoft.com/library/bb611805\(v=office.15\)) methods.</span></span> <span data-ttu-id="fc27c-107">**AddressEntry** オブジェクトが Exchange ユーザーを表している場合、EnumerateGAL は **AddressEntry** オブジェクトのプロパティを公開する **ExchangeUser** オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="fc27c-107">If the **AddressEntry** object represents an Exchange user, EnumerateGAL returns an **ExchangeUser** object that exposes properties of the **AddressEntry** object.</span></span> <span data-ttu-id="fc27c-108">これらを公開するには、[JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\))、[Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\))、[Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\))、[BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\))、[PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) などの ExchangeUser プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="fc27c-108">Use ExchangeUser properties such as [JobTitle](https://msdn.microsoft.com/library/bb645451\(v=office.15\)), [Department](https://msdn.microsoft.com/library/bb623789\(v=office.15\)), [Alias](https://msdn.microsoft.com/library/bb610682\(v=office.15\)), [BusinessTelephoneNumber](https://msdn.microsoft.com/library/bb612294\(v=office.15\)), or [PrimarySmtpAddress](https://msdn.microsoft.com/library/bb645506\(v=office.15\)) to expose them.</span></span>

<span data-ttu-id="fc27c-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="fc27c-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="fc27c-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fc27c-110">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="fc27c-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fc27c-111">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateGAL()
{
    Outlook.AddressList gal =
        Application.Session.GetGlobalAddressList();
    if (gal != null)
    {
        for (int i = 1; 
            i <= Math.Min(100, gal.AddressEntries.Count - 1); i++)
        {
            Outlook.AddressEntry addrEntry =
                gal.AddressEntries[i];
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeUserAddressEntry
                || addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeRemoteUserAddressEntry)
            {
                Outlook.ExchangeUser exchUser =
                    addrEntry.GetExchangeUser();
                Debug.WriteLine(exchUser.Name + " "
                    + exchUser.PrimarySmtpAddress);
            }
            if (addrEntry.AddressEntryUserType ==
                Outlook.OlAddressEntryUserType.
                olExchangeDistributionListAddressEntry)
            {
                Outlook.ExchangeDistributionList exchDL =
                    addrEntry.GetExchangeDistributionList();
                Debug.WriteLine(exchDL.Name + " "
                    + exchDL.PrimarySmtpAddress);
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="fc27c-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="fc27c-112">See also</span></span>

[<span data-ttu-id="fc27c-113">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="fc27c-113">Address book</span></span>](address-book.md)

