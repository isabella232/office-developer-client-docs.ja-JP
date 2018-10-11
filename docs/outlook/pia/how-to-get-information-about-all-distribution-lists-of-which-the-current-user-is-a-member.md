---
title: 現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する
TOCTitle: Get information about all distribution lists of which the current user is a member
ms:assetid: c5be6aa8-8d85-463e-a377-2a4d57e2106b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184638(v=office.15)
ms:contentKeyID: 55119836
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: f98d7a338866624e67d745e66a66e864fb9bbf99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406765"
---
# <a name="get-information-about-all-distribution-lists-of-which-the-current-user-is-a-member"></a><span data-ttu-id="5c914-102">現在のユーザーがメンバーになっているすべての配布リストについての情報を取得する</span><span class="sxs-lookup"><span data-stu-id="5c914-102">Get information about all distribution lists of which the current user is a member</span></span>

<span data-ttu-id="5c914-103">この例では、[GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) メソッドを使用して、現在のユーザーがメンバーになっているすべての配布リストについての情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5c914-103">This example uses the [GetMemberOfList()](https://msdn.microsoft.com/library/bb623397\(v=office.15\)) method to get information about all distribution lists of which the current user is a member.</span></span>

## <a name="example"></a><span data-ttu-id="5c914-104">例</span><span class="sxs-lookup"><span data-stu-id="5c914-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="5c914-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="5c914-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="5c914-106">次の例では、GetCurrentUserMembership で **GetMemberOfList** メソッドを呼び出して、Exchange ユーザーがメンバーになっているすべての配布リストの [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) コレクションを取得します。</span><span class="sxs-lookup"><span data-stu-id="5c914-106">In the following example, GetCurrentUserMembership calls the **GetMemberOfList** method to get an [AddressEntries](https://msdn.microsoft.com/library/bb647650\(v=office.15\)) collection for all distribution lists of which the Exchange user is a member.</span></span> <span data-ttu-id="5c914-107">このユーザーがどの配布リストのメンバーでもない場合、**GetMemberOfList** はカウントが 0 の **AddressEntries** コレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="5c914-107">If the user is not a member of any distribution lists, **GetMemberOfList** returns an **AddressEntries** collection that has a count of zero.</span></span> <span data-ttu-id="5c914-108">ユーザーがオンラインの場合にのみ **GetMemberOfList** は **AddressEntries** コレクションを返します。それ以外の場合、**GetMemberOfList** は null 参照を返します。</span><span class="sxs-lookup"><span data-stu-id="5c914-108">The user must be online for **GetMemberOfList** to return an **AddressEntries** collection; otherwise, **GetMemberOfList** returns a null reference.</span></span> <span data-ttu-id="5c914-109">GetCurrentUserMembership では、現在の [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) オブジェクトを返す [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) メソッドを使用して、ユーザーがオンラインかどうかをテストしています。</span><span class="sxs-lookup"><span data-stu-id="5c914-109">GetCurrentUserMembership uses the [GetExchangeUser()](https://msdn.microsoft.com/library/bb645260\(v=office.15\)) method, which returns the current [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, to test whether the user is online.</span></span> <span data-ttu-id="5c914-110">この例では、アドレス エントリの取得後に、ユーザーの各配布リストに関する情報を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="5c914-110">Once the address entries are obtained, the example writes information about each of the user’s distribution lists to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="5c914-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5c914-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="5c914-112">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5c914-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="5c914-113">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="5c914-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void GetCurrentUserMembership()
{
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        Outlook.ExchangeUser exchUser =
            currentUser.GetExchangeUser();
        if (exchUser != null)
        {
            Outlook.AddressEntries addrEntries =
                exchUser.GetMemberOfList();
            if (addrEntries != null)
            {
                foreach (Outlook.AddressEntry addrEntry
                    in addrEntries)
                {
                    Debug.WriteLine(addrEntry.Name);
                }
            }
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="5c914-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="5c914-114">See also</span></span>

- [<span data-ttu-id="5c914-115">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="5c914-115">Exchange Users</span></span>](exchange-users.md)

