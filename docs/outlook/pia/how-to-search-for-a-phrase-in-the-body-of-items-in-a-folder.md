---
title: フォルダー内のアイテムの本文で語句を検索する
TOCTitle: Search for a phrase in the body of items in a folder
ms:assetid: 2c9f3b5f-ed91-4a07-b247-8f89f00cbc68
ms:mtpsurl: https://msdn.microsoft.com/library/Bb644806(v=office.15)
ms:contentKeyID: 55119924
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dc8e0fb2b82ae9660e292a6ec1dea70e82fe36ef
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722145"
---
# <a name="search-for-a-phrase-in-the-body-of-items-in-a-folder"></a><span data-ttu-id="bdfcd-102">フォルダー内のアイテムの本文で語句を検索する</span><span class="sxs-lookup"><span data-stu-id="bdfcd-102">Search for a phrase in the body of items in a folder</span></span>

<span data-ttu-id="bdfcd-103">この例では、受信トレイ内のアイテムの Body で、文字列 "office" を検索します。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-103">This example searches for the string "office" in the Body of items in the Inbox.</span></span>

## <a name="example"></a><span data-ttu-id="bdfcd-104">例</span><span class="sxs-lookup"><span data-stu-id="bdfcd-104">Example</span></span>

<span data-ttu-id="bdfcd-105">このコード例では、DAV Searching and Locating (DASL) 構文を使用してクエリを指定します。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-105">This code sample uses a DAV Searching and Locating (DASL) syntax to specify a query.</span></span> <span data-ttu-id="bdfcd-106">フィルターを作成するために、このコード例では、まず、既定のストアでクイック検索が有効になっているかどうかを確認しています。これにより、アイテムの本文に含まれる "office" の語句に完全一致する **ci\_phrasematch** キーワードを使用するか、アイテムの本文に出現する "office" と完全に同じ文字列または部分的に同じ文字列に一致する **like** キーワードを使用するかを判断します。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-106">To construct the filter, the code sample first checks if Instant Search is enabled in the default store to determine whether to use the **ci\_phrasematch** keyword for an exact phrase match of "office" in the item body, or the **like** keyword to match any occurrence of "office" as an exact string or a substring in the item body.</span></span> <span data-ttu-id="bdfcd-107">その後で、この例では、受信トレイの [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) メソッドにフィルターを適用して、[Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) オブジェクトで結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-107">The sample then applies the filter to the [GetTable](https://msdn.microsoft.com/library/bb612592\(v=office.15\)) method on the Inbox and obtains the results in a [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object.</span></span> <span data-ttu-id="bdfcd-108">さらに、このコード例では、**Table** で返された各アイテムの件名を表示します。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-108">The code sample then displays the subject of each of the returned items in the **Table**.</span></span>

<span data-ttu-id="bdfcd-109">このコード例では、**Body** プロパティを指定するために、名前空間の表現として urn:schemas:httpmail:textdescription を使用しています。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-109">The code sample specifies the **Body** property by using the namespace representation urn:schemas:httpmail:textdescription.</span></span>

<span data-ttu-id="bdfcd-110">**ci\_phrasematch** キーワードの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-110">The syntax for using the **ci\_phrasematch** keyword is:</span></span>

`<PropertySchemaName> ci_phrasematch <ComparisonString>`

<span data-ttu-id="bdfcd-111">**like** キーワードを使用して先頭一致の検索を行うときの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-111">The syntax for using the **like** keyword for prefix matching is:</span></span>

`<PropertySchemaName> like <Token>%`

<span data-ttu-id="bdfcd-112">**like** キーワードを使用して任意の部分文字列を検索するときの構文は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-112">The syntax for using the **like** keyword for any substring matching is:</span></span>

`<PropertySchemaName> like %<Token>%`

<span data-ttu-id="bdfcd-113">Visual Studio を使用してこのコード例をテストする場合、**Microsoft.Office.Interop.Outlook** 名前空間をインポートするときに、まず Microsoft Outlook 15.0 オブジェクト ライブラリ コンポーネントへの参照を追加し、Outlook 変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-113">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bdfcd-114">**Imports** または **using** ステートメントは、コード例の関数の前に直接置くことはできません。パブリック Class 宣言の前に追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-114">The **Imports** or **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bdfcd-115">次のコード行は、Visual Basic および C\# でインポートおよび割り当てを行う方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bdfcd-115">The following lines of code show how to do the import and assignment in Visual Basic and C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="bdfcd-116">関連項目</span><span class="sxs-lookup"><span data-stu-id="bdfcd-116">See also</span></span>

- [<span data-ttu-id="bdfcd-117">検索とフィルター</span><span class="sxs-lookup"><span data-stu-id="bdfcd-117">Search and filter</span></span>](search-and-filter.md)

