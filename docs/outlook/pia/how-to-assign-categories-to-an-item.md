---
title: 分類項目をアイテムに割り当てる
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 762fd5954e6ec47aed24a9c91b41839f6d292cd9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25407192"
---
# <a name="assign-categories-to-an-item"></a><span data-ttu-id="201f8-102">分類項目をアイテムに割り当てる</span><span class="sxs-lookup"><span data-stu-id="201f8-102">Assign categories to an item</span></span>

<span data-ttu-id="201f8-103">この例では、**Categories** プロパティを使用して、アイテムに分類項目を割り当てる方法を示します。</span><span class="sxs-lookup"><span data-stu-id="201f8-103">This example shows how to assign categories to an item by using its **Categories** property.</span></span>

## <a name="example"></a><span data-ttu-id="201f8-104">例</span><span class="sxs-lookup"><span data-stu-id="201f8-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="201f8-105">次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。</span><span class="sxs-lookup"><span data-stu-id="201f8-105">The following code example is an excerpt from Programming Applications for Microsoft Office Outlook 2007, from  Microsoft Press http://www.microsoft.com/learning/books/default.mspx  (ISBN 9780735622494, copyright Microsoft Press 2007, all rights reserved).</span></span>


<span data-ttu-id="201f8-106">アイテムに分類項目を割り当てるには、アイテムの **Categories** プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="201f8-106">To assign categories to an item, use the particular item's **Categories** property.</span></span> <span data-ttu-id="201f8-107">このコード サンプルは、「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」で定義されている OutlookItem ヘルパー クラスを使用して、OutlookItem.**Categories** プロパティを簡単に呼び出します。最初にアイテムをキャストする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="201f8-107">This code sample makes use of the   helper class, defined in How to: Create a Helper Class to Access Common Outlook Item Members, to conveniently call the   property without having to first cast the item.</span></span> <span data-ttu-id="201f8-108">**Categories** プロパティは、コンマで区切られた 255 文字以内の文字列で表される分類項目を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="201f8-108">The **Categories** property gets or sets categories that are represented by a comma-delimited string that can contain a maximum of 255 characters.</span></span> <span data-ttu-id="201f8-109">各分類項目の値は、コンマと空白文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="201f8-109">The commas and spaces are used to separate the category values.</span></span> <span data-ttu-id="201f8-110">[NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) コレクションに含まれない分類項目を割り当てると、色の表示されない分類項目になります。</span><span class="sxs-lookup"><span data-stu-id="201f8-110">Assigning a category that is not in the [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) collection of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object will result in the category not displaying a color.</span></span>

<span data-ttu-id="201f8-p102">以下のコード例の AssignCategories では、まず、DAV Searching and Locating (DASL) クエリを使用して受信トレイ内のアイテムをフィルター処理し、件名に "ISV" が含まれるアイテムを抽出します。次に、AssignCategories では、**OutlookItem** クラスを使用して、フィルターで抽出されたアイテムを反復処理します。**item.Categories** から返される文字列が null 参照ではなく、既に ISV に割り当てられている場合は、ISV 分類項目がアイテムに割り当てられています。</span><span class="sxs-lookup"><span data-stu-id="201f8-p102">In the following code example, AssignCategories creates a restriction for items that contain “ISV” in the subject by first using a DAV Searching and Locating (DASL) query to filter items in the Inbox that contain “ISV” in the subject. AssignCategories then iterates through the filtered items by using the **OutlookItem** class and, if the string returned by **item.Categories** is not a null reference or was already assigned to the ISV, the ISV category is assigned to the item.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```csharp
private void AssignCategories()
{
    string filter = "@SQL=" + "\"" + "urn:schemas:httpmail:subject"
        + "\"" + " ci_phrasematch 'ISV'";
    Outlook.Items items =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).Items.Restrict(filter);
    for (int i = 1; i <= items.Count; i++)
    {
        OutlookItem item = new OutlookItem(items[i]);
        string existingCategories = item.Categories;
        if (String.IsNullOrEmpty(existingCategories))
        {
            item.Categories = "ISV";
        }
        else
        {
            if (item.Categories.Contains("ISV") == false)
            {
                item.Categories = existingCategories + ", ISV";
            }
        }
        item.Save();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="201f8-113">関連項目</span><span class="sxs-lookup"><span data-stu-id="201f8-113">See also</span></span>

- [<span data-ttu-id="201f8-114">色の分類項目</span><span class="sxs-lookup"><span data-stu-id="201f8-114">Color Categories</span></span>](color-categories.md)
