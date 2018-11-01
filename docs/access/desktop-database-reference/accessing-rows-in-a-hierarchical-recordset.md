---
title: 階層レコード セット内の行へのアクセス
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 3041aa1486f9630a36383dde4ad675c50c799339
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870031"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a><span data-ttu-id="e2c1a-102">階層レコード セット内の行へのアクセス</span><span class="sxs-lookup"><span data-stu-id="e2c1a-102">Accessing rows in a hierarchical Recordset</span></span>

<span data-ttu-id="e2c1a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e2c1a-104">次の例では、階層 [Recordset](recordset-object-ado.md) 内の行へのアクセスに必要な手順を示します。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-104">The following example shows the steps necessary to access rows in a hierarchical [Recordset](recordset-object-ado.md):</span></span>

1. <span data-ttu-id="e2c1a-105">authors および titleauthor テーブルの **Recordset** オブジェクトが、author ID によって関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-105">**Recordset** objects from the authors and titleauthor tables are related by author ID.</span></span>

2. <span data-ttu-id="e2c1a-106">外側のループで、各作成者の姓名、州、および ID が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-106">The outer loop displays each author's first and last name, state, and identification.</span></span>

3. <span data-ttu-id="e2c1a-107">各行に対して追加された **Recordset** が **Fields** コレクションから取得され、*rstTitleAuthor* に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-107">The appended **Recordset** for each row is retrieved from the **Fields** collection and assigned to *rstTitleAuthor*.</span></span>

4. <span data-ttu-id="e2c1a-108">内側のループで、追加された **Recordset** の各行からの 4 つのフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-108">The inner loop displays four fields from each row in the appended **Recordset**.</span></span>

> [!NOTE] 
> <span data-ttu-id="e2c1a-109">[StayInSync](stayinsync-property-ado.md)プロパティは、明示的に変更するには外側のループの各イテレーションでこの章を確認するための説明のため、FALSE に設定されます。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-109">The [StayInSync](stayinsync-property-ado.md) property is set to FALSE for purposes of illustration, so you can see the chapter change explicitly in each iteration of the outer loop.</span></span> <span data-ttu-id="e2c1a-110">ただし、手順 2 にある最初の行の前に手順 3 の割り当て作業を移動すると、割り当てが 1 回だけで済むので、より効率的になります。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-110">However, the example will be more efficient if the assignment in step 3 is moved before the first line in step 2, so that the assignment is performed only once.</span></span> <span data-ttu-id="e2c1a-111">*最初*は暗黙的に、自動的に変更する対応する章を*rst*が新しい行に移動したときに**StayInSync**プロパティを true に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2c1a-111">Set the **StayInSync** property to TRUE, so that *rstTitleAuthor* will implicitly and automatically change to the corresponding chapter whenever *rst* moves to a new row.</span></span>

<span data-ttu-id="e2c1a-112">**例**</span><span class="sxs-lookup"><span data-stu-id="e2c1a-112">**Example**</span></span>

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

