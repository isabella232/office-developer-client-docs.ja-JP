---
title: フォルダー内の非表示のアイテムを列挙する
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: b048ec7fb47a8cbf6b8b49115c59079754fd4ba6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406023"
---
# <a name="enumerate-hidden-items-in-a-folder"></a><span data-ttu-id="2e5c6-102">フォルダー内の非表示のアイテムを列挙する</span><span class="sxs-lookup"><span data-stu-id="2e5c6-102">Enumerate hidden items in a folder</span></span>

<span data-ttu-id="2e5c6-103">この例では、フォルダー内の非表示のアイテムを検索して列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-103">This example shows how to find and enumerate hidden items in a folder.</span></span>

## <a name="example"></a><span data-ttu-id="2e5c6-104">例</span><span class="sxs-lookup"><span data-stu-id="2e5c6-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="2e5c6-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="2e5c6-106">フォルダー内のアイテム セットを表す [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトの機能の 1 つに、非表示のアイテムを持つ機能があります。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-106">One feature of the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, which represents a set of items in a folder, is that it may have hidden items.</span></span> <span data-ttu-id="2e5c6-107">フォルダー内の非表示のアイテムを返すには、[MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトの [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドの *TableContents* パラメーターを [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)) に設定します。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-107">To return hidden items in a folder, set the  *TableContents* parameter in the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method of the [MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) object to [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)) .</span></span> <span data-ttu-id="2e5c6-108">次のコード例の TableForInboxHiddenItems は、受信トレイ フォルダー内の非表示のアイテムを取得し、非表示の各アイテムの [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) プロパティと [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) プロパティの値を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに出力します。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-108">In the following code example,   obtains the hidden items of an Inbox folder, and writes the values of the Subject and MessageClass properties for each hidden item to the trace listeners of the Listeners collection.</span></span>

<span data-ttu-id="2e5c6-109">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-109">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="2e5c6-110">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-110">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="2e5c6-111">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2e5c6-111">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void TableForInboxHiddenItems()
{
    // Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    // Call GetTable with OlTableContents.olHiddenItems
    Outlook.Table table =
        folder.GetTable("",
        Outlook.OlTableContents.olHiddenItems);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        // Test for null subject
        if (nextRow["Subject"] == null)
        {
            Debug.WriteLine(nextRow["MessageClass"]);
        }
        else
        {
            Debug.WriteLine(nextRow["Subject"] + " "
                + nextRow["MessageClass"]);
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="2e5c6-112">関連項目</span><span class="sxs-lookup"><span data-stu-id="2e5c6-112">See also</span></span>

<span data-ttu-id="2e5c6-113">-[検索とフィルター](search-and-filter.md)</span><span class="sxs-lookup"><span data-stu-id="2e5c6-113">Search and Filter</span></span>

