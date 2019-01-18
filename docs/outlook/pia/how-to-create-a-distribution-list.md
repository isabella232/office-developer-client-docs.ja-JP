---
title: 配布リストを作成する
TOCTitle: Create a distribution list
ms:assetid: c1fdbf3d-9669-4721-aabf-e8a332b82e0e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184637(v=office.15)
ms:contentKeyID: 55119841
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f37338209ea468d0143dfd1063c3c57216bc13ea
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721760"
---
# <a name="create-a-distribution-list"></a><span data-ttu-id="f80f1-102">配布リストを作成する</span><span class="sxs-lookup"><span data-stu-id="f80f1-102">Create a distribution list</span></span>

<span data-ttu-id="f80f1-103">この例では、配布リストを作成してそれをユーザーに表示する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-103">This example shows how to create a distribution list and display it to the user.</span></span>

## <a name="example"></a><span data-ttu-id="f80f1-104">例</span><span class="sxs-lookup"><span data-stu-id="f80f1-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="f80f1-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="f80f1-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>


<span data-ttu-id="f80f1-106">次のコード例の CreateDistributionList では、[DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) オブジェクトを作成する [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) メソッドを呼び出すことで、配布リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-106">In the following code example, CreateDistributionList creates a distribution list by calling the [CreateItem(OlItemType)](https://msdn.microsoft.com/library/bb610587\(v=office.15\)) method to create a [DistListItem](https://msdn.microsoft.com/library/bb645382\(v=office.15\)) object.</span></span> <span data-ttu-id="f80f1-107">その後、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを作成し、[GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) メソッドを呼び出して、既定の [連絡先] フォルダー内で [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) プロパティの値が "Top Custome" になっていて [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) プロパティの値が空でない連絡先をすべて検索します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-107">Next it creates a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, and calls the [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612189\(v=office.15\)) method to find all contacts in the default Contacts folder for which the [Subject](https://msdn.microsoft.com/library/bb624088\(v=office.15\)) property value is “Top Customer” and the [Email1Address](https://msdn.microsoft.com/library/bb609902\(v=office.15\)) property value is not empty.</span></span> <span data-ttu-id="f80f1-108">すべての連絡先を特定した後で、**Email1Address** の名前を列として **Table** に追加します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-108">Once all contacts are identified, the **Email1Address** name is added as a column to the **Table**.</span></span> <span data-ttu-id="f80f1-109">その後、CreateDistributionList では、[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトから [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) メソッドを使用して [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-109">CreateDistributionList then creates a [Recipient](https://msdn.microsoft.com/library/bb624370\(v=office.15\)) object by using the [CreateRecipient(String)](https://msdn.microsoft.com/library/bb609962\(v=office.15\)) method from the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object.</span></span> <span data-ttu-id="f80f1-110">最後に、CreateDistributionList では "Top Customers" 配布リストをユーザーに表示します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-110">CreateDistributionList finally displays the “Top Customers” distribution list to the user.</span></span>

> [!NOTE] 
> <span data-ttu-id="f80f1-111">[DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)) オブジェクトの [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) メソッドには、解決済みの **Recipient** オブジェクトをパラメーターとして渡す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f80f1-111">You must pass a resolved **Recipient** object as a parameter to the [AddMember(Recipient)](https://msdn.microsoft.com/library/bb612290(v=office.15)) method of the [DistListItem](https://msdn.microsoft.com/library/bb645382(v=office.15)) object.</span></span> <span data-ttu-id="f80f1-112">**Recipient** オブジェクトを解決するには、[Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-112">To resolve a **Recipient** object, use the [Resolve()](https://msdn.microsoft.com/library/bb624165(v=office.15)) method.</span></span>

<span data-ttu-id="f80f1-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f80f1-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="f80f1-114">**using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f80f1-114">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="f80f1-115">次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f80f1-115">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateDistributionList()
{
    Outlook.DistListItem distList = Application.CreateItem(
        Outlook.OlItemType.olDistributionListItem)
        as Outlook.DistListItem;
    distList.Subject = "Top Customers";
    //Find top customer category in Contacts folder
    string filter = "[Categories] = 'Top Customer'"
        + " AND [Email1Address] <> ''";
    Outlook.Table table =
        Application.Session.GetDefaultFolder
        (Outlook.OlDefaultFolders.olFolderContacts).
        GetTable(filter, Outlook.OlTableContents.olUserItems);
    table.Columns.Add("Email1Address");
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Outlook.Recipient recip =
            Application.Session.CreateRecipient(
            nextRow["Email1Address"].ToString());
        //Resolve the Recipient before calling AddMember
        recip.Resolve();
        distList.AddMember(recip);
    }
    distList.Display(false);
}
```

## <a name="see-also"></a><span data-ttu-id="f80f1-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="f80f1-116">See also</span></span>

- [<span data-ttu-id="f80f1-117">Exchange ユーザー</span><span class="sxs-lookup"><span data-stu-id="f80f1-117">Exchange users</span></span>](exchange-users.md)

