---
title: 最終変更時刻に基づいて受信トレイ内のアイテムを列挙する
TOCTitle: Enumerate items in the Inbox based on the last modification time
ms:assetid: 93a25143-def6-4832-bac2-3744558c2736
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184626(v=office.15)
ms:contentKeyID: 55119920
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0a568209caf172fbab26af1441ba7c208562ae19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320357"
---
# <a name="enumerate-items-in-the-inbox-based-on-the-last-modification-time"></a>最終変更時刻に基づいて受信トレイ内のアイテムを列挙する

この例では、最終変更時刻に基づいて、受信トレイ フォルダー内のアイテムを列挙する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトは、[Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\)) オブジェクトまたは [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトの一連のアイテムを表します。 **Table** を取得するには、**Folder** オブジェクトまたは **Search** オブジェクトの [GetTable(Object, Object)](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドを呼び出します。 返された **Table** 内の各アイテムには、そのアイテムのプロパティの既定のサブセットのみが含まれています。 各 [Row](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) オブジェクトはフォルダー内のアイテムと見なされ、各 [Column](https://msdn.microsoft.com/library/bb609646\(v=office.15\)) オブジェクトはアイテムのプロパティと見なされます。 行の削除、追加、または変更は、**Table** ではサポートされていません。 **Table** 内のアイテムを列挙するには、まず、[EndOfTable](https://msdn.microsoft.com/library/bb647715\(v=office.15\)) プロパティを使用して、現在位置がテーブルの最後かどうかを調べます。 **EndOfTable** が **false** を返した場合は、[GetNextRow()](https://msdn.microsoft.com/library/bb609740\(v=office.15\)) メソッドを使用して、既定数の **Column** オブジェクトが格納されている **Row** を返すようにします。 **EndOfTable** が **true** を返すまで **GetNextRow** を呼び出すことで、前進方向に **Table** の反復処理を続行します。

次のコード例の DemoTableForInbox では、受信トレイの **Table** オブジェクトを取得し、**LastModificationTime** プロパティと [Sort(String, Object)](https://msdn.microsoft.com/library/bb652667\(v=office.15\)) メソッドを使用して **Table** オブジェクトを並べ替えてから、テーブルを反復処理して各アイテムの件名を [Listeners](https://msdn.microsoft.com/library/system.diagnostics.debug.listeners.aspx) コレクションのトレース リスナーに書き込みます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoTableForInbox()
{
    //Obtain Inbox
    Outlook.Folder folder =
        Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox)
        as Outlook.Folder;
    //Obtain Table using defaults
    Outlook.Table table =
        folder.GetTable(Type.Missing, Type.Missing);
    table.Sort("LastModificationTime",
        Outlook.OlSortOrder.olDescending);
    while (!table.EndOfTable)
    {
        Outlook.Row nextRow = table.GetNextRow();
        Debug.WriteLine(nextRow["Subject"]);
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

