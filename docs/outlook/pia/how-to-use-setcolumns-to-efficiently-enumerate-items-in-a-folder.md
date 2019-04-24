---
title: SetColumns を使用してフォルダーのアイテムを効率よく列挙する
TOCTitle: Use SetColumns to efficiently enumerate items in a folder
ms:assetid: cd7c7758-8a9c-4f1c-a49c-9305d75be341
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184641(v=office.15)
ms:contentKeyID: 55119921
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: bdfccc6432d35b6f39564e4c87404cc57b6ea27e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338039"
---
# <a name="use-setcolumns-to-efficiently-enumerate-items-in-a-folder"></a>SetColumns を使用してフォルダーのアイテムを効率よく列挙する

この例では、[Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) コレクションの列挙のパフォーマンスを向上するために、 [SetColumns(String)](https://msdn.microsoft.com/library/bb610268\(v=office.15\)) メソッドを使用してコレクションの各アイテムの特定のプロパティをキャッシュする方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

コレクションのアイテムを列挙するには、 **SetColumns** メソッドを使用して、 **Items** コレクションのプロパティをキャッシュします。 **SetColumns** は、プロパティ名を示すコンマ区切り文字列を引数に取ります。コレクションのすべてのアイテムの列挙が終了したら、 [ResetColumns()](https://msdn.microsoft.com/library/bb624355\(v=office.15\)) メソッドを呼び出してプロパティ キャッシュをクリアします。

次のコード サンプルでは、EnumerateContactsWithSetColumns が **SetColumns** メソッドを使用して、連絡先フォルダー内のアイテムの [FileAs](https://msdn.microsoft.com/library/bb647792\(v=office.15\))、[CompanyName](https://msdn.microsoft.com/library/bb610212\(v=office.15\))、[JobTitle](https://msdn.microsoft.com/library/bb609294\(v=office.15\)) のそれぞれのプロパティをキャッシュします。 制限内の空の文字列または null 参照をテストする必要があることに注意してください。

Outlook フォルダーは異なる型のアイテムを含む場合がありますので、注意してください。 このコード サンプルは「[ヘルパー クラスを作成し、Outlook アイテムの共通メンバーにアクセスする](how-to-create-a-helper-class-to-access-common-outlook-item-members.md)」で定義されている OutlookItem ヘルパー クラスを使用します。これは、アイテムを連絡先アイテムと推測する前に、OutlookItem.Class プロパティを簡単に呼び出して、フォルダー内のアイテムのフィルター処理されたサブセットの各項目のメッセージ クラスを確認することを目的としています。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

