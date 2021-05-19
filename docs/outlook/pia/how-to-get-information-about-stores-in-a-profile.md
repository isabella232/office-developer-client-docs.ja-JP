---
title: プロファイルのストアに関する情報を取得する
TOCTitle: Get information about stores in a profile
ms:assetid: e88222d2-e1b7-4393-aac4-5ce9d24d5d5b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184648(v=office.15)
ms:contentKeyID: 55119893
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2044fc52370bdadd5c7f01debbd02c88dd881715
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349421"
---
# <a name="get-information-about-stores-in-a-profile"></a><span data-ttu-id="96734-102">プロファイルのストアに関する情報を取得する</span><span class="sxs-lookup"><span data-stu-id="96734-102">Get information about stores in a profile</span></span>

<span data-ttu-id="96734-103">この例では、プロファイル内のストアを取得して列挙する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="96734-103">This example shows how to get and enumerate stores in a profile.</span></span>

## <a name="example"></a><span data-ttu-id="96734-104">例</span><span class="sxs-lookup"><span data-stu-id="96734-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="96734-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="96734-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="96734-106">[Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) コレクションを使用して、特定のプロファイルのストアを列挙できます。</span><span class="sxs-lookup"><span data-stu-id="96734-106">You can use the [Stores](https://msdn.microsoft.com/library/bb622944\(v=office.15\)) collection to enumerate the stores for a given profile.</span></span> <span data-ttu-id="96734-107">**Stores** コレクションは、各 [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) オブジェクトに関する情報 (現在のプロファイルで **Store** オブジェクトがいつ追加されたか、 **Store** オブジェクトがいつ削除されるか、など) を公開するメンバーを提供します。</span><span class="sxs-lookup"><span data-stu-id="96734-107">The **Stores** collection provides members that expose information about each [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object, such as when a **Store** object has been added or when a **Store** object is about to be removed in the current profile.</span></span> <span data-ttu-id="96734-108">次のコード例の EnumerateStores は、現在のプロファイル内のストアを表す **Stores** オブジェクトを取得し、ストアを列挙します。</span><span class="sxs-lookup"><span data-stu-id="96734-108">In the following code example, EnumerateStores gets the **Stores** object that represents stores in the current profile, and enumerates the stores.</span></span> <span data-ttu-id="96734-109">EnumerateStores は、**Stores** コレクション内の各 **Store** オブジェクトを調べます。</span><span class="sxs-lookup"><span data-stu-id="96734-109">EnumerateStores examines each **Store** object in the **Stores** collection.</span></span> <span data-ttu-id="96734-110">[IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) プロパティの値が **true** (.pst または .ost ストアであることを示す) の場合は、 [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) プロパティと [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) プロパティが [ Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに出力されます。</span><span class="sxs-lookup"><span data-stu-id="96734-110">If the [IsDataFileStore](https://msdn.microsoft.com/library/bb624116\(v=office.15\)) property returns **true**, indicating that it is a .pst or .ost store, the [DisplayName](https://msdn.microsoft.com/library/bb612209\(v=office.15\)) and [FilePath](https://msdn.microsoft.com/library/bb646113\(v=office.15\)) properties are written to the trace listeners in the [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) collection.</span></span>

<span data-ttu-id="96734-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="96734-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="96734-112">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="96734-112">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="96734-113">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="96734-113">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateStores()
{
    Outlook.Stores stores = Application.Session.Stores;
    foreach (Outlook.Store store in stores)
    {
        if (store.IsDataFileStore == true)
        {
            Debug.WriteLine(String.Format("Store: "
            + store.DisplayName
            + "\n" + "File Path: "
            + store.FilePath + "\n"));
        }
    }
}
```

## <a name="see-also"></a><span data-ttu-id="96734-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="96734-114">See also</span></span>

- [<span data-ttu-id="96734-115">ストア</span><span class="sxs-lookup"><span data-stu-id="96734-115">Stores</span></span>](stores.md)

