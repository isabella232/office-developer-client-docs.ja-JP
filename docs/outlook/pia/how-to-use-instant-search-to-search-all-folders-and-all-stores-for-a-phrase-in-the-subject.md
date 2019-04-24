---
title: クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335372"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a>クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索する

この例では、クイック検索を使用して、すべてのフォルダーとすべてのストアから件名の特定の語句を検索し、該当するアイテムをエクスプローラー ウィンドウに表示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード サンプルは、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

クイック検索は、クエリを発行することで検索できるようになる Microsoft Outlook の機能であり、コンテンツに基づいた結果が返されます。 クエリが処理されると、さまざまなオブジェクト ([Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクト、[Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) コレクション、[Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) オブジェクトなど) で結果が返されます。 クイック検索を使用するコードは、Microsoft Windows デスクトップ サーチによって提供される、高度な検索テクニック (AQS) を使用することで記述できます。 AQS は、Outlook でサポートされる 3 つのクエリ言語のうちの 1 つです。 強力なものではありますが、[Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) オブジェクトの [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) メソッドに限定されます。 **Table** オブジェクトまたは **Item** オブジェクトに制限するために AQS を使用することはできません。 さらに、AQS クエリで返された結果が表示できるのは、Outlook ユーザー インターフェイスのみです。 次の表に、Outlook でサポートされる 3 つのクエリ言語の一覧を示します。ただし、このトピックでは、AQS の使用についてのみ説明します。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>クエリ言語</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AQS</p></td>
<td><p>AQS は Windows デスクトップ サーチで使用され、Outlook のクイック検索機能を実現するクエリ言語です。</p></td>
</tr>
<tr class="even">
<td><p>DASL</p></td>
<td><p>DAV Search and Locating (DASL) は、Outlook における Microsoft Exchange の DASL 実装に基づくクエリ言語です。DASL を使用すると、 <b>Table</b> オブジェクトで結果を返すことができます。  </p></td>
</tr>
<tr class="odd">
<td><p>Jet</p></td>
<td><p>Jet は、Outlook 用の簡単なクエリ言語で、Microsoft Jet Expression サービスに基づいています。Jet を使用して <b>Items</b> コレクションや <b>Table</b> オブジェクトの <b>Restrict</b> メソッドのためのフィルター文字列が作成されます。  </p></td>
</tr>
</tbody>
</table>


次のコード例では、DemoInstantSearch は、[Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) オブジェクトの [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) プロパティを使用してインデックス作成が有効化されているすべてのストア内にあるメール フォルダーをすべて取得します。 その後で、**Explorer** オブジェクトの **Search** メソッドを使用して、件名内に "Office 2007" と完全一致する語句が含まれている、先月受信したアイテムのすべてを抽出します。 検索の結果は、最終的に別のエクスプローラー ウィンドウに表示されます。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

