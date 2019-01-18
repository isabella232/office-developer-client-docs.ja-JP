---
title: クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709440"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a><span data-ttu-id="ebd27-102">クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する</span><span class="sxs-lookup"><span data-stu-id="ebd27-102">Use instant search to search all folders and all stores for a phrase in the subject</span></span>

<span data-ttu-id="ebd27-103">この例では、クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索し、該当するアイテムをエクスプローラー ウィンドウに表示します。</span><span class="sxs-lookup"><span data-stu-id="ebd27-103">This example uses Instant Search to search all folders and all stores for a phrase in the subject, and then displays the items in an explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="ebd27-104">例</span><span class="sxs-lookup"><span data-stu-id="ebd27-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ebd27-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="ebd27-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="ebd27-106">クイック検索は、クエリを発行することで検索できるようになる Microsoft Outlook の機能であり、コンテンツに基づいた結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="ebd27-106">Instant Search is a feature of Microsoft Outlook that enables you to search by issuing queries that return results based on the content.</span></span> <span data-ttu-id="ebd27-107">クエリが処理されると、さまざまなオブジェクト ([Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクト、[Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) コレクション、[Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトなど) で結果が返されます。</span><span class="sxs-lookup"><span data-stu-id="ebd27-107">Once your query has been processed, the results can be returned in a variety of objects, including the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection, and the [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="ebd27-108">クイック検索を使用するコードは、Microsoft Windows デスクトップ サーチによって提供される、高度な検索テクニック (AQS) を使用することで記述できます。</span><span class="sxs-lookup"><span data-stu-id="ebd27-108">You can write code that uses Instant Search by using the Advanced Query Syntax (AQS) that is offered by Microsoft Windows Desktop Search.</span></span> <span data-ttu-id="ebd27-109">AQS は、Outlook でサポートされる 3 つのクエリ言語のうちの 1 つです。</span><span class="sxs-lookup"><span data-stu-id="ebd27-109">AQS is one of three query languages that Outlook supports.</span></span> <span data-ttu-id="ebd27-110">強力なものではありますが、[Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトの [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) メソッドに限定されます。</span><span class="sxs-lookup"><span data-stu-id="ebd27-110">It is powerful, but limited to the [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="ebd27-111">**Table** オブジェクトまたは **Item** オブジェクトに制限するために AQS を使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="ebd27-111">You cannot use AQS to provide a restriction for **Table** or **Item** objects.</span></span> <span data-ttu-id="ebd27-112">さらに、AQS クエリで返された結果が表示できるのは、Outlook ユーザー インターフェイスのみです。</span><span class="sxs-lookup"><span data-stu-id="ebd27-112">In addition, the results returned by an AQS query can be displayed only in the Outlook user interface.</span></span> <span data-ttu-id="ebd27-113">次の表に、Outlook でサポートされる 3 つのクエリ言語の一覧を示します。ただし、このトピックでは、AQS の使用についてのみ説明します。</span><span class="sxs-lookup"><span data-stu-id="ebd27-113">The following table lists the three query languages that Outlook supports; however, this topic will illustrate the use of only AQS.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ebd27-114">クエリ言語</span><span class="sxs-lookup"><span data-stu-id="ebd27-114">Query language</span></span></p></th>
<th><p><span data-ttu-id="ebd27-115">説明</span><span class="sxs-lookup"><span data-stu-id="ebd27-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ebd27-116">AQS</span><span class="sxs-lookup"><span data-stu-id="ebd27-116">AQS</span></span></p></td>
<td><p><span data-ttu-id="ebd27-117">AQS は Windows デスクトップ サーチで使用され、Outlook のクイック検索機能を実現するクエリ言語です。</span><span class="sxs-lookup"><span data-stu-id="ebd27-117">AQS is used by Windows Desktop Search and is the query language for the Instant Search feature in Outlook.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ebd27-118">DASL</span><span class="sxs-lookup"><span data-stu-id="ebd27-118">DASL</span></span></p></td>
<td><p><span data-ttu-id="ebd27-p102">DAV Search and Locating (DASL) は、Outlook における Microsoft Exchange の DASL 実装に基づくクエリ言語です。DASL を使用すると、 <b>Table</b> オブジェクトで結果を返すことができます。  </span><span class="sxs-lookup"><span data-stu-id="ebd27-p102">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook. DASL can be used to return results in the <b>Table</b> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ebd27-121">Jet</span><span class="sxs-lookup"><span data-stu-id="ebd27-121">Jet</span></span></p></td>
<td><p><span data-ttu-id="ebd27-p103">Jet は、Outlook 用の簡単なクエリ言語で、Microsoft Jet Expression サービスに基づいています。Jet を使用して <b>Items</b> コレクションや <b>Table</b> オブジェクトの <b>Restrict</b> メソッドのためのフィルター文字列が作成されます。  </span><span class="sxs-lookup"><span data-stu-id="ebd27-p103">Jet query language provides a simple query language for Outlook, and is based on the Microsoft Jet Expression Service. Jet is used to create filter strings for the <b>Restrict</b> methods of the <b>Items</b> collection and the <b>Table</b> object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ebd27-124">次のコード例では、DemoInstantSearch は、[Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) オブジェクトの [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) プロパティを使用してインデックス作成が有効化されているすべてのストア内にあるメール フォルダーをすべて取得します。</span><span class="sxs-lookup"><span data-stu-id="ebd27-124">In the following code example, DemoInstantSearch gets all mail folders in all stores where indexing is enabled by using the [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) property of the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="ebd27-125">その後で、**Explorer** オブジェクトの **Search** メソッドを使用して、件名内に "Office 2007" と完全一致する語句が含まれている、先月受信したアイテムのすべてを抽出します。</span><span class="sxs-lookup"><span data-stu-id="ebd27-125">It then uses the **Search** method of the **Explorer** object to filter for all items that contain the exact phrase “Office 2007” in the subject and that have been received in the last month.</span></span> <span data-ttu-id="ebd27-126">検索の結果は、最終的に別のエクスプローラー ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="ebd27-126">The results of the search are finally displayed in a separate explorer window.</span></span>

<span data-ttu-id="ebd27-127">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebd27-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="ebd27-128">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ebd27-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="ebd27-129">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ebd27-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="ebd27-130">関連項目</span><span class="sxs-lookup"><span data-stu-id="ebd27-130">See also</span></span>

- [<span data-ttu-id="ebd27-131">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="ebd27-131">Search and filter</span></span>](search-and-filter.md)

