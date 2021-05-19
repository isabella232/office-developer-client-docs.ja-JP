---
title: 現在のユーザーの上司の直属部下についての情報を取得する
TOCTitle: Get information about direct reports of the current user's manager
ms:assetid: 768bf573-1b10-4776-8947-a7f8dc3ebde0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184617(v=office.15)
ms:contentKeyID: 55119842
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d49e96138d8cd2d857c49cc293258e1493afc747
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349435"
---
# <a name="get-information-about-direct-reports-of-the-current-users-manager"></a><span data-ttu-id="3241b-102">現在のユーザーの上司の直属部下についての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="3241b-102">Get information about direct reports of the current user's manager</span></span>

<span data-ttu-id="3241b-103">この例では、現在のユーザーに上司がいる場合はその上司の直属の部下を取得し、上司の各直属部下についての情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="3241b-103">This example gets the direct reports of the current user’s manager, if any, and then displays information about each of the manager’s direct reports.</span></span>

## <a name="example"></a><span data-ttu-id="3241b-104">例</span><span class="sxs-lookup"><span data-stu-id="3241b-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="3241b-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="3241b-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="3241b-106">次の例の GetManagerDirectReports プロシージャでは、[GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) メソッドを呼び出して、[ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトで表されるユーザーの上司を取得します。</span><span class="sxs-lookup"><span data-stu-id="3241b-106">In the following example, the GetManagerDirectReports procedure calls the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method to get the user’s manager, represented by an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object.</span></span> <span data-ttu-id="3241b-107">現在のユーザーに上司がいる場合は、[AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) コレクションを返す [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) を呼び出します。このコレクションは、ユーザーの上司のすべての直属の部下のアドレス エントリを表します。</span><span class="sxs-lookup"><span data-stu-id="3241b-107">If the current user has a manager, [GetDirectReports()](https://msdn.microsoft.com/library/bb647204\(v=office.15\)) is called to return an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection that represents the address entries for all the direct reports of user’s manager.</span></span> <span data-ttu-id="3241b-108">上司に直属の部下がいない場合、**GetDirectReports** はカウントがゼロの **AddressEntries** コレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="3241b-108">If the manager has no direct reports, **GetDirectReports** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="3241b-109">上司の直属の部下を取得した後、GetManagerDirectReports では上司の各直属の部下に関する情報を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="3241b-109">Once the manager’s direct reports are obtained, GetManagerDirectReports writes information about each of the manager’s direct reports to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>


> [!NOTE]
> <span data-ttu-id="3241b-110">このメソッドが **AddressEntries** コレクションを返すには、サインインしているユーザーがオンラインになっている必要があります。それ以外の場合、**GetDirectReports** は null 参照を返します。</span><span class="sxs-lookup"><span data-stu-id="3241b-110">The signed-in user must be online for this method to return an **AddressEntries** collection; otherwise, **GetDirectReports** returns a null reference.</span></span> <span data-ttu-id="3241b-111">実稼働用のコードについては、[\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) プロパティ (複数の Exchange シナリオでは [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) プロパティ) を使用してユーザーがオフライン状態であるかどうかをテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3241b-111">For production code, you must test for the user being offline by using the [\_NameSpace.ExchangeConnectionMode](https://msdn.microsoft.com/library/bb647638(v=office.15)) property, or the [\_Account.ExchangeConnectionMode](https://msdn.microsoft.com/library/ff185249(v=office.15)) property for multiple Exchange scenarios.</span></span>

<span data-ttu-id="3241b-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3241b-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="3241b-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3241b-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="3241b-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="3241b-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetManagerDirectReports()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser manager =
            currentUser.GetExchangeUser().GetExchangeUserManager();
        if (manager != null)
        {
            Outlook.AddressEntries addrEntries =
                manager.GetDirectReports();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Outlook.ExchangeUser exchUser =
                        addrEntry.GetExchangeUser();
                    StringBuilder sb = new StringBuilder();
                    sb.AppendLine("Name: "
                        + exchUser.Name);
                    sb.AppendLine("Title: "
                        + exchUser.JobTitle);
                    sb.AppendLine("Department: "
                        + exchUser.Department);
                    sb.AppendLine("Location: "
                        + exchUser.OfficeLocation);
                    Debug.WriteLine(sb.ToString());
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="3241b-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="3241b-115">See also</span></span>

- [<span data-ttu-id="3241b-116">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="3241b-116">Exchange users</span></span>](exchange-users.md)

