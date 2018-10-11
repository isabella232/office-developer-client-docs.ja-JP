---
title: フォルダー内のアイテムの本文で語句を検索する
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2792e5bd96547975d878f89a7e186c24c4983d8f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406933"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a>フォルダー内のアイテムの本文で語句を検索する

この例では、受信トレイ内のアイテムの Body で、文字列 "office" を検索します。

## <a name="example"></a>例

このコード例では、DAV Searching and Locating (DASL) 構文を使用してクエリを指定します。 フィルターを作成するために、このコード例では、まず、既定のストアでクイック検索が有効になっているかどうかを確認しています。これにより、アイテムの本文に含まれる "office" の語句に完全一致する **ci\_phrasematch** キーワードを使用するか、アイテムの本文に出現する "office" と完全に同じ文字列または部分的に同じ文字列に一致する **like** キーワードを使用するかを判断します。 その後で、この例では、受信トレイの [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドにフィルターを適用して、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトで結果を取得します。 さらに、このコード例では、**Table** で返された各アイテムの件名を表示します。

このコード例では、**Body** プロパティを指定するために、名前空間の表現として urn:schemas:httpmail:textdescription を使用しています。

**ci\_phrasematch** キーワードの構文は次のとおりです。

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

**like** キーワードを使用して先頭一致の検索を行うときの構文は次のとおりです。

`<PropertySchemaName> like <Token>%`

**like** キーワードを使用して任意の部分文字列を検索するときの構文は次のとおりです。

`<PropertySchemaName> like %<Token>%`

Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。 **Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。 次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```


```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```vb
Private Sub DemoSearchBody()
    Dim filter As String
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " ci_phrasematch 'office'"
    Else
        filter = "@SQL=" & Chr(34) _
            & "urn:schemas:httpmail:textdescription" & Chr(34) _
            & " like '%office%'"
    End If
    Dim table As Outlook.Table = _
        Application.Session.GetDefaultFolder( _
        Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
        filter, Outlook.OlTableContents.olUserItems)
    While Not (table.EndOfTable)
        Dim row As Outlook.Row = table.GetNextRow()
        Debug.WriteLine(row("Subject"))
    End While
End Sub
```


```csharp
private void DemoSearchBody()
{
    string filter;
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " ci_phrasematch 'office'";
    }
    else
    {
        filter = "@SQL=" + "\""
            + "urn:schemas:httpmail:textdescription" + "\""
            + " like '%office%'";
    }
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

