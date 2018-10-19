---
title: SetColumns を使用してフォルダーのアイテムを効率よく列挙する
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2e75a0cb06420f5072805cdf03ad8f7925670e67
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407472"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a><span data-ttu-id="6ce96-102">SetColumns を使用してフォルダーのアイテムを効率よく列挙する</span><span class="sxs-lookup"><span data-stu-id="6ce96-102">Use SetColumns to efficiently enumerate items in a folder</span></span>

<span data-ttu-id="6ce96-103">この例では、[Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) コレクションの列挙のパフォーマンスを向上するために、 [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) メソッドを使用してコレクションの各アイテムの特定のプロパティをキャッシュする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6ce96-103">This example shows how to improve the performance of enumerating the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection by using the [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) method to cache certain properties of each item in the collection.</span></span>

## <a name="example"></a><span data-ttu-id="6ce96-104">例</span><span class="sxs-lookup"><span data-stu-id="6ce96-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="6ce96-105">次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="6ce96-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>

<span data-ttu-id="6ce96-p101">コレクションのアイテムを列挙するには、 **SetColumns** メソッドを使用して、 **Items** コレクションのプロパティをキャッシュします。 **SetColumns** は、プロパティ名を示すコンマ区切り文字列を引数に取ります。コレクションのすべてのアイテムの列挙が終了したら、 [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) メソッドを呼び出してプロパティ キャッシュをクリアします。</span><span class="sxs-lookup"><span data-stu-id="6ce96-p101">To enumerate items in a collection, use the **SetColumns** method to cache properties on the **Items** collection. **SetColumns** takes an argument that is a comma-delimited string that represents property names. Once all items in the collection have been enumerated, call the [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) method to clear the property cache.</span></span>

<span data-ttu-id="6ce96-109">次のコード サンプルでは、EnumerateContactsWithSetColumns が **SetColumns** メソッドを使用して、連絡先フォルダー内のアイテムの [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\))、[CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\))、[JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) のそれぞれのプロパティをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="6ce96-109">In the following code example,   uses the SetColumns method to cache the FileAs , CompanyName , and JobTitle properties of items in the Contacts folder.</span></span> <span data-ttu-id="6ce96-110">制限内の空の文字列または null 参照をテストする必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="6ce96-110">Note that you must test for empty strings or a null reference in the restriction.</span></span>

<span data-ttu-id="6ce96-111">Outlook フォルダーは異なる型のアイテムを含む場合がありますので、注意してください。</span><span class="sxs-lookup"><span data-stu-id="6ce96-111">Note that an Outlook folder can possibly contain items of different types.</span></span> <span data-ttu-id="6ce96-112">このコード サンプルは「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」で定義されている OutlookItem ヘルパー クラスを使用します。これは、アイテムを連絡先アイテムと推測する前に、OutlookItem.Class プロパティを簡単に呼び出して、フォルダー内のアイテムのフィルター処理されたサブセットの各項目のメッセージ クラスを確認することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="6ce96-112">Note that an Outlook folder can possibly contain items of different types. This code sample makes use of the OutlookItem helper class, defined in How to: Create a Helper Class to Access Common Outlook Item Members, to conveniently call the OutlookItem.Class property to verify the message class of each item in the filtered subset of items in the folder, before assuming the item is a contact item.</span></span>

<span data-ttu-id="6ce96-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6ce96-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the   variable when you import the Microsoft.Office.Interop.Outlook namespace.</span></span> <span data-ttu-id="6ce96-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6ce96-114">The using statement must not occur directly before the functions in the code example but must be added before the public   declaration.</span></span> <span data-ttu-id="6ce96-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="6ce96-115">The following line of code shows how to do the import and assignment in C#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void EnumerateContactsWithSetColumns()
{
    // Obtain Contacts folder
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderContacts)
        as Outlook.Folder;
    string filter = "Not([CompanyName] Is Null)" +
        " AND Not([JobTitle] Is Null)";
    Outlook.Items items = folder.Items.Restrict(filter);
    items.SetColumns("FileAs, CompanyName, JobTitle");
    for (int i = 1; i <= items.Count; i++)
    {
        // Create an instance of OutlookItem
        OutlookItem myItem = new OutlookItem(items[i]);
        if (myItem.Class == Outlook.OlObjectClass.olContact)
        {
            // Use InnerObject to return ContactItem
            Outlook.ContactItem contact =
                myItem.InnerObject as Outlook.ContactItem;
            StringBuilder sb = new StringBuilder();
            sb.AppendLine(contact.FileAs);
            sb.AppendLine(contact.CompanyName);
            sb.AppendLine(contact.JobTitle);
            sb.AppendLine();
            Debug.WriteLine(sb.ToString());
        }
    }
    items.ResetColumns();
}
```

## <a name="see-also"></a><span data-ttu-id="6ce96-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="6ce96-116">See also</span></span>

- [<span data-ttu-id="6ce96-117">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="6ce96-117">Search and Filter</span></span>](search-and-filter.md)

