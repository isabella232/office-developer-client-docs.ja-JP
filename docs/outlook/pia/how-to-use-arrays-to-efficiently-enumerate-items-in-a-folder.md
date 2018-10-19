---
title: 配列を使用してフォルダーのアイテムを効率よく列挙する
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d165b27da58a4e99eabb897aac3d2dc03811f588
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407507"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="da9f2-102">配列を使用してフォルダーのアイテムを効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="da9f2-102">Use arrays to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="da9f2-103">この例では、[GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) メソッドを使用して [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトのアイテムを効率的に列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="da9f2-103">This example shows how to efficiently enumerate items in a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) object by using the [GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) method.</span></span>

## <a name="example"></a><span data-ttu-id="da9f2-104">例</span><span class="sxs-lookup"><span data-stu-id="da9f2-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="da9f2-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="da9f2-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="da9f2-106">次のコード例の DemoGetArrayForTable では、[GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドを使用して、**Folder** オブジェクトから [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを取得します。</span><span class="sxs-lookup"><span data-stu-id="da9f2-106">In the following code example,   gets a Table object from a Folder object by using the GetTable(Object, Object) method.</span></span> <span data-ttu-id="da9f2-107">DemoGetArrayForTable は次に、**GetArray** メソッドを使用して、テーブルの各行の要素を含む [Array](https://msdn.microsoft.com/library/system.array.aspx) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="da9f2-107"> then uses the GetArray method to return an Array object that contains elements for every row in the table.</span></span> <span data-ttu-id="da9f2-108">返される **Array** オブジェクトは、**Table** の行の値と列の値の組み合わせを表す 2 次元配列です。</span><span class="sxs-lookup"><span data-stu-id="da9f2-108">The returned **Array** object is a two-dimensional array that represents a set of row and column values from the **Table**.</span></span> <span data-ttu-id="da9f2-109">配列は、1 から始める Outlook コレクションの場合とは違い、0 から始まります。</span><span class="sxs-lookup"><span data-stu-id="da9f2-109">The array is zero-based, instead of one-based as is the case with Outlook collections.</span></span> <span data-ttu-id="da9f2-110">**Array** オブジェクトを取得したら、このコードは for ループを使用してテーブルを列挙します。</span><span class="sxs-lookup"><span data-stu-id="da9f2-110">Once the Array object is obtained, the code uses a   loop to enumerate through the table.</span></span>

<span data-ttu-id="da9f2-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="da9f2-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="da9f2-112">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="da9f2-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="da9f2-113">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="da9f2-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="da9f2-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="da9f2-114">See also</span></span>

- [<span data-ttu-id="da9f2-115">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="da9f2-115">Search and Filter</span></span>](search-and-filter.md)

