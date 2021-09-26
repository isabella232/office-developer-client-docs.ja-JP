---
title: 分類項目をアイテムに割り当てる
TOCTitle: Assign categories to an item
ms:assetid: 4070801b-994a-46df-91fe-4efca834886e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424469(v=office.15)
ms:contentKeyID: 55119828
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 1e095837a25b07053e2f590fdabbd63d4baa5d70
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619385"
---
# <a name="assign-categories-to-an-item"></a>分類項目をアイテムに割り当てる

この例では、**Categories** プロパティを使用して、アイテムに分類項目を割り当てる方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。


アイテムに分類項目を割り当てるには、アイテムの **Categories** プロパティを使用します。 このコード サンプルは、「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」で定義されている OutlookItem ヘルパー クラスを使用して、OutlookItem.**Categories** プロパティを簡単に呼び出します。最初にアイテムをキャストする必要はありません。 **Categories** プロパティは、コンマで区切られた 255 文字以内の文字列で表される分類項目を取得または設定します。 各分類項目の値は、コンマと空白文字で区切られます。 [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) オブジェクトの [Categories](https://msdn.microsoft.com/library/bb646607\(v=office.15\)) コレクションに含まれない分類項目を割り当てると、色の表示されない分類項目になります。

以下のコード例の AssignCategories では、まず、DAV Searching and Locating (DASL) クエリを使用して受信トレイ内のアイテムをフィルター処理し、件名に "ISV" が含まれるアイテムを抽出します。次に、AssignCategories では、**OutlookItem** クラスを使用して、フィルターで抽出されたアイテムを反復処理します。**item.Categories** から返される文字列が null 参照ではなく、既に ISV に割り当てられている場合は、ISV 分類項目がアイテムに割り当てられています。

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

## <a name="see-also"></a>関連項目

- [色の分類項目](color-categories.md)

