---
title: フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する
TOCTitle: Search attachments of items in a folder for an exact phrase
ms:assetid: 3202c0c7-ee3d-4396-b3a9-d24990b44829
ms:mtpsurl: https://msdn.microsoft.com/library/Bb609825(v=office.15)
ms:contentKeyID: 55119889
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f237a2268fd287e96959dfc0522103b47e55d37b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28698296"
---
# <a name="search-attachments-of-items-in-a-folder-for-an-exact-phrase"></a><span data-ttu-id="068ac-102">フォルダー内のアイテムの添付ファイルで完全に一致する語句を検索する</span><span class="sxs-lookup"><span data-stu-id="068ac-102">Search attachments of items in a folder for an exact phrase</span></span>

<span data-ttu-id="068ac-103">この例では、受信トレイ内のアイテムへの添付ファイルで、文字列 "office" を完全一致で検索します。</span><span class="sxs-lookup"><span data-stu-id="068ac-103">This example searches for the exact search string "office" in attachments to items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="068ac-104">例</span><span class="sxs-lookup"><span data-stu-id="068ac-104">Example</span></span>

<span data-ttu-id="068ac-105">このコード例では、DAV Searching and Locating (DASL) 構文を使用してクエリを指定します。</span><span class="sxs-lookup"><span data-stu-id="068ac-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="068ac-106">フィルターを作成するために、まずクイック検索が既定のストアで有効になっているかどうかをチェックし、添付ファイル内で "office" を完全一致で検索する **ci\_phrasematch** キーワードを使用するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="068ac-106">To construct the filter, the code sample first checks whether Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match to "office" in any attachment.</span></span> <span data-ttu-id="068ac-107">その後で、この例では、受信トレイの [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドにフィルターを適用して、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトで結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="068ac-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="068ac-108">さらに、このコード例では、**Table** で返された各アイテムの件名を表示します。</span><span class="sxs-lookup"><span data-stu-id="068ac-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="068ac-109">このコード例では、アイテムの **Attachments** プロパティを指定するために、名前空間の表現として https://schemas.microsoft.com/mapi/proptag/0x0EA5001E を使用しています。</span><span class="sxs-lookup"><span data-stu-id="068ac-109">The code sample specifies the **Attachments** property of an item using the namespace representation, https://schemas.microsoft.com/mapi/proptag/0x0EA5001E.</span></span> <span data-ttu-id="068ac-110">**ci\_phrasematch** キーワードの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="068ac-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="068ac-111">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="068ac-111">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="068ac-112">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="068ac-112">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="068ac-113">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="068ac-113">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E"
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
        "https://schemas.microsoft.com/mapi/proptag/0x0EA5001E";
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

## <a name="see-also"></a><span data-ttu-id="068ac-114">関連項目</span><span class="sxs-lookup"><span data-stu-id="068ac-114">See also</span></span>

- [<span data-ttu-id="068ac-115">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="068ac-115">Search and filter</span></span>](search-and-filter.md)

