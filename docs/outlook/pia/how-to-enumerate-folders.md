---
title: フォルダーを列挙する
TOCTitle: Enumerate folders
ms:assetid: 564730f9-3da3-4eff-b207-64ac4fec632d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184607(v=office.15)
ms:contentKeyID: 55119855
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 91165754ccd86ebff07ec99e60f0ad1a167dea05
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406254"
---
# <a name="enumerate-folders"></a><span data-ttu-id="88303-102">フォルダーを列挙する</span><span class="sxs-lookup"><span data-stu-id="88303-102">Enumerate folders</span></span>

<span data-ttu-id="88303-103">この例では、フォルダーのコレクションを反復処理することでフォルダーを列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="88303-103">This example shows how to enumerate folders by iterating through a collection of folders.</span></span>

## <a name="example"></a><span data-ttu-id="88303-104">例</span><span class="sxs-lookup"><span data-stu-id="88303-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="88303-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="88303-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="88303-106">次のコード例では、まず EnumerateFoldersInDefaultStore メソッドが [GetRootFolder()](https://msdn.microsoft.com/library/bb645807\(v=office.15\)) メソッドを使用して、既定のストアのルート フォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="88303-106">In the following code example, the   method first obtains the root folder for the default store by using the GetRootFolder() method.</span></span> <span data-ttu-id="88303-107">次に、ルート フォルダーで EnumerateFolders メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="88303-107">It then calls the   method on the root folder.</span></span> <span data-ttu-id="88303-108">EnumerateFolders はルート フォルダーを取得し、ルート フォルダーが表している既定のストアのフォルダーをウォークスルーします。</span><span class="sxs-lookup"><span data-stu-id="88303-108"> takes in a root folder and walks through the folders of the default store that the root folder represents.</span></span> <span data-ttu-id="88303-109">EnumerateFolders は、まず [Folders](https://msdn.microsoft.com/library/bb646854\(v=office.15\)) プロパティを使用してルートの [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトのサブフォルダーを取得します。</span><span class="sxs-lookup"><span data-stu-id="88303-109"> first uses the Folders property to obtain the subfolders of the root Folder object.</span></span> <span data-ttu-id="88303-110">次に、階層内のすべてのフォルダーを列挙するために、EnumerateFolders が繰り返し呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="88303-110"> is then called recursively to enumerate all the folders in a hierarchy.</span></span> <span data-ttu-id="88303-111">最後に、EnumerateFolders は各 **Folder** の [FolderPath](https://msdn.microsoft.com/library/bb647409\(v=office.15\)) プロパティを [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクション内のトレース リスナーに書き込みます。</span><span class="sxs-lookup"><span data-stu-id="88303-111">Finally,   writes the FolderPath property of each Folder to the trace listeners in the Listeners collection.</span></span>

<span data-ttu-id="88303-112">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="88303-112">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="88303-113">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88303-113">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="88303-114">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="88303-114">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateFoldersInDefaultStore()
{
    Outlook.Folder root =
        Application.Session.
        DefaultStore.GetRootFolder() as Outlook.Folder;
    EnumerateFolders(root);
}

// Uses recursion to enumerate Outlook subfolders.
private void EnumerateFolders(Outlook.Folder folder)
{
    Outlook.Folders childFolders =
        folder.Folders;
    if (childFolders.Count > 0)
    {
        foreach (Outlook.Folder childFolder in childFolders)
        {
            // Write the folder path.
            Debug.WriteLine(childFolder.FolderPath);
            // Call EnumerateFolders using childFolder.
            EnumerateFolders(childFolder);
        }
    }
}               
```

## <a name="see-also"></a><span data-ttu-id="88303-115">関連項目</span><span class="sxs-lookup"><span data-stu-id="88303-115">See also</span></span>

- [<span data-ttu-id="88303-116">フォルダー</span><span class="sxs-lookup"><span data-stu-id="88303-116">Folders</span></span>](folders.md)

