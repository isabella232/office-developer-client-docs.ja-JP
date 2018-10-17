---
title: アクティブ エクスプローラーで選択した項目を表示する
TOCTitle: Display selected items in the active Explorer
ms:assetid: 31bb217b-8b45-4b50-942e-b6c2a7f13c83
ms:mtpsurl: https://msdn.microsoft.com/library/Dn292517(v=office.15)
ms:contentKeyID: 55119844
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: d2599aff01afc7cc02797210a260befdfb72be33
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405505"
---
# <a name="display-selected-items-in-the-active-explorer"></a><span data-ttu-id="ed961-102">アクティブ エクスプローラーで選択した項目を表示する</span><span class="sxs-lookup"><span data-stu-id="ed961-102">Display selected items in the active Explorer</span></span>

<span data-ttu-id="ed961-103">この例では、OutlookItem ヘルパー クラスを利用して、アクティブなエクスプローラー ウィンドウで選択したすべてのアイテムを簡単に表示する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ed961-103">This example shows how to use the OutlookItem helper class to conveniently display all the items selected in the active Explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="ed961-104">例</span><span class="sxs-lookup"><span data-stu-id="ed961-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="ed961-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="ed961-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="ed961-106">[Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) オブジェクトには、アクティブな Outlook エクスプローラーで現在選択されている Outlook アイテムのセットが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ed961-106">The [Selection](https://msdn.microsoft.com/library/bb612099\(v=office.15\)) object contains the set of Outlook items currently selected in the active Outlook explorer.</span></span> <span data-ttu-id="ed961-107">[ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)) で表されるアクティブなエクスプローラーも、選択されたアイテムのセットも、選択されているアイテムの種類を示しません。</span><span class="sxs-lookup"><span data-stu-id="ed961-107">Neither the active explorer, represented by [ActiveExplorer()](https://msdn.microsoft.com/library/bb647410\(v=office.15\)) , nor the set of selected items indicates the type of the items that are selected.</span></span> <span data-ttu-id="ed961-108">通常、最初にアイテムの種類を識別して、その種類に応じた固有の **Display** メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed961-108">Normally, you would have to first identify the item type and then call the specific **Display** method for that type.</span></span> <span data-ttu-id="ed961-109">**Display** メソッドはすべての Outlook アイテム オブジェクトに共通していて、このメソッドは OutlookItem ヘルパー クラスに含まれているため、このヘルパー クラスを利用して、OutlookItem オブジェクトのインスタンスである myItem を宣言すると、myItem.Display を使用して選択された各アイテムを表示できます。</span><span class="sxs-lookup"><span data-stu-id="ed961-109">Because the Display method is common to all Outlook items objects and the   helper class includes this method, you can take advantage of the helper class, by declaring an instance of the   object,  , and using   to display each item in the selection.</span></span> <span data-ttu-id="ed961-110">OutlookItem ヘルパー クラスの実装方法は、「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ed961-110">You can see the implementation of the   helper class in How to: Create a Helper Class to Access Common Outlook Item Members</span></span>

<span data-ttu-id="ed961-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="ed961-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="ed961-112">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ed961-112">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="ed961-113">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="ed961-113">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DisplaySelectedItems()
{
    Outlook.Selection selection =
        Application.ActiveExplorer().Selection;
    for (int i = 1; i <= selection.Count; i++)
    {
        OutlookItem myItem = new OutlookItem(selection[i]);
        myItem.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="ed961-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="ed961-114">See also</span></span>

- [<span data-ttu-id="ed961-115">ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする</span><span class="sxs-lookup"><span data-stu-id="ed961-115">Create a Helper class to access common Outlook item members</span></span>](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)
- [<span data-ttu-id="ed961-116">Outlook アイテム全般</span><span class="sxs-lookup"><span data-stu-id="ed961-116">General Outlook Items</span></span>](general-outlook-items.md)
