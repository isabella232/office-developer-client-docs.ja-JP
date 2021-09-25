---
title: 階層レコードセット内の行へのアクセス
TOCTitle: Accessing rows in a hierarchical Recordset
ms:assetid: db59b152-b780-539c-17ef-462e8adfb26e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15)
ms:contentKeyID: 48548104
ms.date: 10/17/2018
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: fd50934eeaf91149f59262a45e9585602ffb73e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586314"
---
# <a name="accessing-rows-in-a-hierarchical-recordset"></a>階層レコードセット内の行へのアクセス

**適用先**: Access 2013、Office 2013

次の例では、階層 [Recordset](recordset-object-ado.md) 内の行へのアクセスに必要な手順を示します。

1. authors および titleauthor テーブルの **Recordset** オブジェクトが、author ID によって関連付けられます。

2. 外側のループで、各作成者の姓名、州、および ID が表示されます。

3. 各行に対して追加された **Recordset** が **Fields** コレクションから取得され、*rstTitleAuthor* に割り当てられます。

4. 内側のループで、追加された **Recordset** の各行からの 4 つのフィールドが表示されます。

> [!NOTE] 
> [図を示す目的で StayInSync](stayinsync-property-ado.md)プロパティは FALSE に設定されています。そのため、外側ループの各反復で章の変更を明示的に確認できます。 ただし、手順 2 にある最初の行の前に手順 3 の割り当て作業を移動すると、割り当てが 1 回だけで済むので、より効率的になります。 **StayInSync** プロパティを TRUE に設定すると *、rstTitleAuthor* は *、rst* が新しい行に移動するたびに、暗黙的に自動的に対応するチャプターに変更されます。

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

