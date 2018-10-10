---
title: 階層 Recordset 内の行にアクセスする
TOCTitle: Accessing Rows in a Hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a7596341f96c7df1d51e67721aacd15f8b075f25
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479394"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="6ec26-102">階層 Recordset 内の行にアクセスする</span><span class="sxs-lookup"><span data-stu-id="6ec26-102">Accessing Rows in a Hierarchical Recordset</span></span>


<span data-ttu-id="6ec26-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="6ec26-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6ec26-104">次の例では、階層 [Recordset](recordset-object-ado.md) 内の行へのアクセスに必要な手順を示します。</span><span class="sxs-lookup"><span data-stu-id="6ec26-104">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

1.  <span data-ttu-id="6ec26-105">authors および titleauthor テーブルの **Recordset** オブジェクトが、author ID によって関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="6ec26-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2.  <span data-ttu-id="6ec26-106">外側のループで、各作成者の姓名、州、および ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ec26-106">The outer loop displays each author's first and last name, state, and identification.</span></span>

3.  <span data-ttu-id="6ec26-107">各行に対して追加された **Recordset** が **Fields** コレクションから取得され、*rstTitleAuthor* に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="6ec26-107">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4.  <span data-ttu-id="6ec26-108">内側のループで、追加された **Recordset** の各行からの 4 つのフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6ec26-108">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

<span data-ttu-id="6ec26-109">[StayInSync](stayinsync-property-ado.md) プロパティが説明のために FALSE に設定されているので、外側ループのそれぞれの繰り返しの中で、明示的なチャプターの変化を確認できます。</span><span class="sxs-lookup"><span data-stu-id="6ec26-109">(The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration — so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="6ec26-110">ただし、手順 2 にある最初の行の前に手順 3 の割り当て作業を移動すると、割り当てが 1 回だけで済むので、より効率的になります。</span><span class="sxs-lookup"><span data-stu-id="6ec26-110">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="6ec26-111">**StayInSync**プロパティ TRUE に設定、*最初*は暗黙的に、自動的に変更に対応する章*rst*が新しい行に移動したときにできるようにします。)</span><span class="sxs-lookup"><span data-stu-id="6ec26-111">Then set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.)</span></span>

<span data-ttu-id="6ec26-112">**例**</span><span class="sxs-lookup"><span data-stu-id="6ec26-112">**Example**</span></span>

```vb 
 
Sub datashape() 
 Dim cnn As New ADODB.Connection 
 Dim rst As New ADODB.Recordset 
 Dim rstTitleAuthor As New ADODB.Recordset 
 
 cnn.Provider = "MSDataShape" 
 cnn.Open "Data Provider=MSDASQL;" & _ 
 "Data Source=SRV;" & _ 
 "User Id=MyUserName;Password=MyPassword;Database=Pubs" 
' STEP 1 
 rst.StayInSync = FALSE 
 rst.Open "SHAPE {select * from authors} " & _ 
 "APPEND ({select * from titleauthor} " & _ 
 "RELATE au_id TO au_id) AS chapTitleAuthor", _ 
 cnn 
' STEP 2 
 While Not rst.EOF 
 Debug.Print rst("au_fname"), rst("au_lname"), _ 
 rst("state"), rst("au_id") 
' STEP 3 
 Set rstTitleAuthor = rst("chapTitleAuthor").Value 
' STEP 4 
 While Not rstTitleAuthor.EOF 
 Debug.Print rstTitleAuthor(0), rstTitleAuthor(1), _ 
 rstTitleAuthor(2), rstTitleAuthor(3) 
 rstTitleAuthor.MoveNext 
 Wend 
 rst.MoveNext 
 Wend 
End Sub 
```

