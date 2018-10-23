---
title: 先月に変更された受信トレイアイテムをフィルター処理して表示する
TOCTitle: Filter and display Inbox items modified in the last month
ms:assetid: ef6004dc-0b5a-4d1f-8937-1384d1dfc1ca
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424482(v=office.15)
ms:contentKeyID: 55119886
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 952d28cc64ffa3638f8147b665e88a372dc81848
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406877"
---
# <a name="filter-and-display-inbox-items-modified-in-the-last-month"></a>先月に変更された受信トレイアイテムをフィルター処理して表示する

この例では、先月に変更された受信トレイアイテムをフィルター処理して表示する方法を示します。

## <a name="example"></a>例

> [!NOTE] 
> 次のコード例は、『[Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493)』からの抜粋です。

DAV Search and Locating (DASL) は、Outlook における Microsoft Exchange の DASL 実装に基づくクエリ言語です。 [表](https://msdn.microsoft.com/library/bb652856\(v=office.15\))オブジェクトに示されるように、フォルダーのデータ内のプロパティに基づくアイテム レベルの検索結果などを戻すのに使用することができます。 DASL フィルターは、等号 (=) 演算子による文字列の比較 (同値、接頭辞、語句、部分文字列の一致) をサポートしています。 DASL クエリを使用して、日付と時刻の比較とフィルター処理を行うことができます。

DASL クエリによる **DateTime** 比較は常に協定世界時 (UTC) で行われるので、クエリを正しく動作させるためには現地時刻を UTC に変換する必要があります。さらに、 **DateTime** 値を文字列表現に変換する必要もあります。DASL フィルターでは文字列による比較が行われるからです。 **DateTime** の変換には次の 2 つの方法があります。1 つは [Row](https://msdn.microsoft.com/library/bb645832\(v=office.15\)) オブジェクトの [LocalTimeToUTC(Object)](https://msdn.microsoft.com/library/bb610126\(v=office.15\)) メソッドによる変換で、もう 1 つは Outlook の **DateTime** マクロによる変換です。

次のコードは、 **LocalTimeToUTC** メソッドを使用して **LastModificationTime** プロパティ (すべての **Item** オブジェクトにある既定の列) の値を UTC に変換する方法を示しています。

```csharp
DateTime modified = nextRow.LocalTimeUTC(“LastModificationTime”);
```

次の表は、 **DateTime** プロパティの値と UTC の相対日時を比較して文字列をフィルター処理するための **DateTime** マクロです。 SchemaName のプロパティの値は、名前空間で参照される有効な **DateTime** プロパティを表します。

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>マクロ</p></th>
<th><p>構文</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>today</p></td>
<td><p>%today(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティの値が今日と等しいアイテムに制限します。</p></td>
</tr>
<tr class="even">
<td><p>tomorrow</p></td>
<td><p>%tomorrow(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティの値が明日と等しいアイテムに制限します。</p></td>
</tr>
<tr class="odd">
<td><p>yesterday</p></td>
<td><p>%yesterday(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティの値が昨日と等しいアイテムに制限します。</p></td>
</tr>
<tr class="even">
<td><p>next7days</p></td>
<td><p>%next7days(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティの値の範囲が次の 7 日間と等しいアイテムに制限します。</p></td>
</tr>
<tr class="odd">
<td><p>last7days</p></td>
<td><p>%last7days(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティの値の範囲が今日までの 7 日間と等しいアイテムに制限します。</p></td>
</tr>
<tr class="even">
<td><p>nextweek</p></td>
<td><p>%nextweek(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティ値の範囲が来週と等しいアイテムに制限します。</p></td>
</tr>
<tr class="odd">
<td><p>thisweek</p></td>
<td><p>%thisweek(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティ値の範囲が今週と等しいアイテムに制限します。</p></td>
</tr>
<tr class="even">
<td><p>lastweek</p></td>
<td><p>%lastweek(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティ値の範囲が先週と等しいアイテムに制限します。</p></td>
</tr>
<tr class="odd">
<td><p>nextmonth</p></td>
<td><p>%nextmonth(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティ値の範囲が来月と等しいアイテムに制限します。</p></td>
</tr>
<tr class="even">
<td><p>thismonth</p></td>
<td><p>%thismonth(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティ値の範囲が今月と等しいアイテムに制限します。</p></td>
</tr>
<tr class="odd">
<td><p>lastmonth</p></td>
<td><p>%lastmonth(“SchemaName”)%</p></td>
<td><p>抽出対象を SchemaName プロパティ値の範囲が先月と等しいアイテムに制限します。</p></td>
</tr>
</tbody>
</table>


次の例では、DemoDASLDateMacro が **lastmonthDateTime**マクロを使用する DASL クエリを作成し、先月変更されたユーザーの受信トレイ内のアイテムをフィルター処理します。 次に、作成、**表**オブジェクトをフィルターと共に作成、列挙し、制限された**テーブル**オブジェクトの行を表示します。

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリッククラス宣言の前に追加する必要があります。 次のコード行は、C\# でインポートおよび割り当てを行う方法を示しています。

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoDASLDateMacro()
{
    string filter = "@SQL=" + "%lastmonth(" + "\"" +
        "DAV:getlastmodified" + "\"" + ")%";
    Outlook.Table table = Application.Session.GetDefaultFolder(
        Outlook.OlDefaultFolders.olFolderInbox).GetTable(
        filter, Outlook.OlTableContents.olUserItems);
    while (!table.EndOfTable)
    {
        Outlook.Row row = table.GetNextRow();
        Debug.WriteLine(row["Subject"]);
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)

