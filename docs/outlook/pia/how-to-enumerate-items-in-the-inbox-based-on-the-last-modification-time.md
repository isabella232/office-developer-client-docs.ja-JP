---
title: 最終変更時刻に基づいて受信トレイ内のアイテムを列挙する
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320357"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a><span data-ttu-id="8f988-102">最終変更時刻に基づいて受信トレイ内のアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="8f988-102">Enumerate items in the Inbox based on the last modification time</span></span>

<span data-ttu-id="8f988-103">この例では、最終変更時刻に基づいて、受信トレイ フォルダー内のアイテムを列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="8f988-103">This example shows how to enumerate items in the Inbox folder based on the last modification time.</span></span>

## <a name="example"></a><span data-ttu-id="8f988-104">例</span><span class="sxs-lookup"><span data-stu-id="8f988-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="8f988-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="8f988-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="8f988-106">[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトは、[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトまたは [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトの一連のアイテムを表します。</span><span class="sxs-lookup"><span data-stu-id="8f988-106">The [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object represents a set of items from a [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) or [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="8f988-107">**Table** を取得するには、**Folder** オブジェクトまたは **Search** オブジェクトの [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8f988-107">To obtain a **Table**, call the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on a **Folder** or **Search** object.</span></span> <span data-ttu-id="8f988-108">返された **Table** 内の各アイテムには、そのアイテムのプロパティの既定のサブセットのみが含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f988-108">Each item in the returned **Table** contains only a default subset of the item’s properties.</span></span> <span data-ttu-id="8f988-109">各 [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) オブジェクトはフォルダー内のアイテムと見なされ、各 [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) オブジェクトはアイテムのプロパティと見なされます。</span><span class="sxs-lookup"><span data-stu-id="8f988-109">Each [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) object can be regarded as an item in the folder, and each [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) object as a property of an item.</span></span> <span data-ttu-id="8f988-110">行の削除、追加、または変更は、**Table** ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="8f988-110">Removing, adding, or changing rows is not supported in the **Table**.</span></span> <span data-ttu-id="8f988-111">**Table** 内のアイテムを列挙するには、まず、[EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) プロパティを使用して、現在位置がテーブルの最後かどうかを調べます。</span><span class="sxs-lookup"><span data-stu-id="8f988-111">To enumerate items in a **Table**, first use the [EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) property to see whether your current position is at the end of the table.</span></span> <span data-ttu-id="8f988-112">**EndOfTable** が **false** を返した場合は、[GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) メソッドを使用して、既定数の **Column** オブジェクトが格納されている **Row** を返すようにします。</span><span class="sxs-lookup"><span data-stu-id="8f988-112">If **EndOfTable** returns **false**, use the [GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) method to return a **Row**, which contains a default number of **Column** objects.</span></span> <span data-ttu-id="8f988-113">**EndOfTable** が **true** を返すまで **GetNextRow** を呼び出すことで、前進方向に **Table** の反復処理を続行します。</span><span class="sxs-lookup"><span data-stu-id="8f988-113">You continue iterating in a forward manner through the **Table** by calling **GetNextRow** until **EndOfTable** returns **true**.</span></span>

<span data-ttu-id="8f988-114">次のコード例の DemoTableForInbox では、受信トレイの **Table** オブジェクトを取得し、**LastModificationTime** プロパティと [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) メソッドを使用して **Table** オブジェクトを並べ替えてから、テーブルを反復処理して各アイテムの件名を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="8f988-114">In the following code example, DemoTableForInbox obtains a **Table** object for the Inbox folder, sorts the **Table** object by using the **LastModificationTime** property and [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) method, and iterates through the table to write the subject of each item to the trace listeners of the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="8f988-115">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="8f988-115">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="8f988-116">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f988-116">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="8f988-117">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f988-117">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a><span data-ttu-id="8f988-118">関連項目</span><span class="sxs-lookup"><span data-stu-id="8f988-118">See also</span></span>

- [<span data-ttu-id="8f988-119">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="8f988-119">Search and filter</span></span>](search-and-filter.md)

