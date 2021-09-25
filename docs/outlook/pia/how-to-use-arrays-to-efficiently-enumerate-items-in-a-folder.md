---
title: 配列を使用してフォルダーのアイテムを効率よく列挙する
TOCTitle: Use arrays to efficiently enumerate items in a folder
ms:assetid: 05a73225-ad0d-4d52-90b6-448d220348df
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184588(v=office.15)
ms:contentKeyID: 55119885
ms.date: 07/24/2014
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dbe2852de11c34401e1653d8e2b0b25d36e19b37
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560467"
---
# <a name="use-arrays-to-efficiently-enumerate-items-in-a-folder"></a>配列を使用してフォルダーのアイテムを効率よく列挙する

この例では、[GetArray(Int32)](https://msdn.microsoft.com/library/bb608928\(v=office.15\)) メソッドを使用して [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトのアイテムを効率的に列挙する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

次のコード例の DemoGetArrayForTable では、[GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドを使用して、**Folder** オブジェクトから [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトを取得します。 DemoGetArrayForTable は次に、**GetArray** メソッドを使用して、テーブルの各行の要素を含む [Array](https://msdn.microsoft.com/library/system.array.aspx) オブジェクトを返します。 返される **Array** オブジェクトは、**Table** の行の値と列の値の組み合わせを表す 2 次元配列です。 配列は、1 から始める Outlook コレクションの場合とは違い、0 から始まります。 **Array** オブジェクトを取得したら、このコードは for ループを使用してテーブルを列挙します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoGetArrayForTable()
{
    // Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    Outlook.Table table =
        folder.GetTable("", Outlook.OlTableContents.olUserItems);
    Array tableArray = table.GetArray(table.GetRowCount()) as Array;
    for (int i = 0; i <= tableArray.GetUpperBound(0); i++)
    {
        for (int j = 0; j <= tableArray.GetUpperBound(1); j++)
        {
            Debug.WriteLine(tableArray.GetValue(i, j));
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

