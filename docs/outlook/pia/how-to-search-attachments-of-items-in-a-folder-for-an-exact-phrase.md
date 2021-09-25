---
title: フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://docs.microsoft.com/office/client-developer/outlook/pia/how-to-search-attachments-of-items-in-a-folder-for-an-exact-phrase?redirectedfrom=MSDN
ms:contentKeyID: 55119889
ms.date: 09/14/2021
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 932af6a8af1ee6a1f6be93f0aff4f3c7267fc151
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623650"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a>フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する

この例では、受信トレイ内のアイテムへの添付ファイルで、文字列 "office" を完全一致で検索します。

## <a name="example"></a>例

このコード例では、DAV Searching and Locating (DASL) 構文を使用してクエリを指定します。 フィルターを作成するために、まずクイック検索が既定のストアで有効になっているかどうかをチェックし、添付ファイル内で "office" を完全一致で検索する **ci\_phrasematch** キーワードを使用するかどうかを決定します。 その後で、この例では、受信トレイの [GetTable](/dotnet/api/microsoft.office.interop.outlook.mapifolder.gettable.md) メソッドにフィルターを適用して、[Table](/dotnet/api/microsoft.office.interop.outlook.table.md) オブジェクトで結果を取得します。 さらに、このコード例では、**Table** で返された各アイテムの件名を表示します。

このコード例では、アイテムの **Attachments** プロパティを指定するために、名前空間の表現として https://schemas.microsoft.com/mapi/proptag/0x0EA5001E を使用しています。 **ci\_phrasematch** キーワードの構文は次のとおりです。

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

Visual Studio を使用してこのコード サンプルをテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートする際に、最初に必ず Microsoft Outlook 15.0 Object Library コンポーネントへの参照を追加し、そして Outlook 変数を指定します。**Imports** または **using** ステートメントは、コード サンプル中の関数の前に直接置かれず、Public クラス宣言の前に追加する必要があります。次のプログラムは、Visual Basic および C\#でインポートおよび割り当てを行う方法を示しています。

```vb
Imports Outlook = Microsoft.Office.Interop.Outlook
```

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```

```vb
Private Sub DemoSearchAttachments()
    Dim filter As String
    Const PR_SEARCH_ATTACHMENTS As String = _
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
    If (Application.Session.DefaultStore.IsInstantSearchEnabled) Then
        filter = "@SQL=" & Chr(34) _
            & PR_SEARCH_ATTACHMENTS & Chr(34) _
            & " ci_phrasematch 'office'"
        Dim table As Outlook.Table = _
            Application.Session.GetDefaultFolder( _
            Outlook.OlDefaultFolders.olFolderInbox).GetTable( _
            filter, Outlook.OlTableContents.olUserItems)
        While Not (table.EndOfTable)
            Dim row As Outlook.Row = table.GetNextRow()
            Debug.WriteLine(row("Subject"))
        End While
    End If
End Sub
```

```csharp
private void DemoSearchAttachments()
{
    string filter;
    const string PR_SEARCH_ATTACHMENTS =
        "http://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        filter = "@SQL=" + "\""
            + PR_SEARCH_ATTACHMENTS + "\""
            + " ci_phrasematch 'office'";
        Outlook.Table table = Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox).GetTable(
            filter, Outlook.OlTableContents.olUserItems);
        while (!table.EndOfTable)
        {
            Outlook.Row row = table.GetNextRow();
            Debug.WriteLine(row["Subject"]);
        }
    }
}
```

## <a name="see-also"></a>関連項目

- [検索とフィルター](search-and-filter.md)
