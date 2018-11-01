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
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>階層レコード セット内の行へのアクセス

**適用されます**Access 2013、Office 2013。

次の例では、階層 [Recordset](recordset-object-ado.md) 内の行へのアクセスに必要な手順を示します。

1. authors および titleauthor テーブルの **Recordset** オブジェクトが、author ID によって関連付けられます。

2. 外側のループで、各作成者の姓名、州、および ID が表示されます。

3. 各行に対して追加された **Recordset** が **Fields** コレクションから取得され、*rstTitleAuthor* に割り当てられます。

4. 内側のループで、追加された **Recordset** の各行からの 4 つのフィールドが表示されます。

> [!NOTE] 
> [StayInSync](stayinsync-property-ado.md)プロパティは、明示的に変更するには外側のループの各イテレーションでこの章を確認するための説明のため、FALSE に設定されます。 ただし、手順 2 にある最初の行の前に手順 3 の割り当て作業を移動すると、割り当てが 1 回だけで済むので、より効率的になります。 *最初*は暗黙的に、自動的に変更する対応する章を*rst*が新しい行に移動したときに**StayInSync**プロパティを true に設定します。

**例**

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

