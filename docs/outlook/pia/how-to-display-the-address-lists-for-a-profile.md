---
title: プロファイルのアドレス一覧を表示する
TOCTitle: Display the address lists for a profile
ms:assetid: ced8230b-110b-4ccb-a699-588798144154
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184643(v=office.15)
ms:contentKeyID: 55119802
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b69ed930241dc058b22b75c6ccc9121f8856d28f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703721"
---
# <a name="display-the-address-lists-for-a-profile"></a><span data-ttu-id="46e69-102">プロファイルのアドレス一覧を表示する</span><span class="sxs-lookup"><span data-stu-id="46e69-102">Display the address lists for a profile</span></span>

<span data-ttu-id="46e69-103">この例では、現在のプロファイルのアドレス一覧を表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="46e69-103">This example shows how to display the address lists for the current profile.</span></span>

## <a name="example"></a><span data-ttu-id="46e69-104">例</span><span class="sxs-lookup"><span data-stu-id="46e69-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="46e69-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="46e69-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="46e69-p101">現在のプロファイルには、[AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) コレクションで表されたアドレス一覧が含まれます。 AddressLists コレクションのインスタンスを取得するには、 [NameSpace](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) オブジェクトの [AddressLists](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) プロパティを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46e69-p101">The current profile contains address lists that are represented by the [AddressLists](https://msdn.microsoft.com/library/bb611894\(v=office.15\)) collection. To get an instance of the AddressLists collection, you must use the [AddressLists](https://msdn.microsoft.com/library/bb624048\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span>

<span data-ttu-id="46e69-108">次のコード例の EnumerateAddressLists は、最初に foreach ステートメントを使用して AddressLists コレクション内の各 [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) オブジェクトを列挙します。</span><span class="sxs-lookup"><span data-stu-id="46e69-108">In the following code example, EnumerateAddressLists first enumerates each [AddressList](https://msdn.microsoft.com/library/bb623538\(v=office.15\)) object in the AddressLists collection by using a foreach statement.</span></span> <span data-ttu-id="46e69-109">次に、[Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\))、[ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\))、[IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\))、および [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) の各プロパティの値を含む文字列を作成します。</span><span class="sxs-lookup"><span data-stu-id="46e69-109">The example then creates a string that contains the values of the [Name](https://msdn.microsoft.com/library/bb609849\(v=office.15\)), [ResolutionOrder](https://msdn.microsoft.com/library/bb646853\(v=office.15\)), [IsReadOnly](https://msdn.microsoft.com/library/bb612676\(v=office.15\)), and [IsInitialAddressList](https://msdn.microsoft.com/library/bb646646\(v=office.15\)) properties.</span></span> <span data-ttu-id="46e69-110">最後に、文字列を EnumerateAddressLists が [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="46e69-110">Finally, EnumerateAddressLists writes the string to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span> <span data-ttu-id="46e69-111">これにより、現在のプロファイルの各アドレス一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="46e69-111">This displays each address list for the current profile.</span></span>

<span data-ttu-id="46e69-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="46e69-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="46e69-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="46e69-113">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="46e69-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="46e69-114">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void EnumerateAddressLists()
{
    Outlook.AddressLists addrLists =
         Application.Session.AddressLists;
    foreach (Outlook.AddressList addrList in addrLists)
    {
        StringBuilder sb = new StringBuilder();
        sb.AppendLine("Display Name: " + addrList.Name);
        sb.AppendLine("Resolution Order: "
            + addrList.ResolutionOrder.ToString());
        sb.AppendLine("Read-only : "
            + addrList.IsReadOnly.ToString());
        sb.AppendLine("Initial Address List: "
            + addrList.IsInitialAddressList.ToString());
        sb.AppendLine("");
        Debug.WriteLine(sb.ToString());
    }
}
```

## <a name="see-also"></a><span data-ttu-id="46e69-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="46e69-115">See also</span></span>

- [<span data-ttu-id="46e69-116">アドレス帳</span><span class="sxs-lookup"><span data-stu-id="46e69-116">Address book</span></span>](address-book.md)

