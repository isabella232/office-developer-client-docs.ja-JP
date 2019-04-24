---
title: フォルダー内の非表示のアイテムを列挙する
TOCTitle: Enumerate hidden items in a folder
ms:assetid: dafad1fb-94ce-4584-b5d1-2de5fad2f72a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184645(v=office.15)
ms:contentKeyID: 55119888
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6508ea955ad74b49b5fef73352b4a1706d8e338c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357408"
---
# <a name="enumerate-hidden-items-in-a-folder"></a>フォルダー内の非表示のアイテムを列挙する

この例では、フォルダー内の非表示のアイテムを検索して列挙する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

フォルダー内のアイテム セットを表す [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトの機能の 1 つに、非表示のアイテムを持つ機能があります。 フォルダー内の非表示のアイテムを返すには、[MAPIFolder](https://msdn.microsoft.com/library/bb624369\(v=office.15\)) オブジェクトの [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドの *TableContents* パラメーターを [olHiddenItems](https://msdn.microsoft.com/library/bb622801\(v=office.15\)) に設定します。 次のコード例の TableForInboxHiddenItems は、受信トレイ フォルダー内の非表示のアイテムを取得し、非表示の各アイテムの [Subject](https://msdn.microsoft.com/library/bb611353\(v=office.15\)) プロパティと [MessageClass](https://msdn.microsoft.com/library/bb645845\(v=office.15\)) プロパティの値を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに出力します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

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

## <a name="see-also"></a>関連項目

-[検索とフィルター](search-and-filter.md)

