---
<<<<<<< ヘッド タイトル: 階層レコード セットの TOCTitle の行へのアクセス: 階層レコード セットの ms:assetid の行へのアクセス: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 09/18/2015 mtps_version: v=office.15
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a>階層 Recordset 内の行にアクセスする

=== タイトル: 階層レコード セットの TOCTitle 内の行へのアクセス: 階層レコード セットの ms:assetid 内の行へのアクセス: db59b152-b780-539c-17ef-462e8adfb26e ms:mtpsurl: https://msdn.microsoft.com/library/JJ250106(v=office.15) ms:contentKeyID: 48548104 ms.date: 2018/10/17 mtps_version: v =office.15
---

# <a name="accessing-rows-in-a-hierarchical-recordset"></a>階層レコード セット内の行へのアクセス
>>>>>>> master

**適用されます**Access 2013 |。Office 2013

次の例では、階層 [Recordset](recordset-object-ado.md) 内の行へのアクセスに必要な手順を示します。

<<<<<<< ヘッド
1.  authors および titleauthor テーブルの **Recordset** オブジェクトが、author ID によって関連付けられます。

2.  外側のループで、各作成者の姓名、州、および ID が表示されます。

3.  各行に対して追加された **Recordset** が **Fields** コレクションから取得され、*rstTitleAuthor* に割り当てられます。

4.  内側のループで、追加された **Recordset** の各行からの 4 つのフィールドが表示されます。

<a name="the-stayinsyncstayinsync-property-adomd-property-is-set-to-false-for-purposes-of-illustration--so-you-can-see-the-chapter-change-explicitly-in-each-iteration-of-the-outer-loop-however-the-example-will-be-more-efficient-if-the-assignment-in-step-3-is-moved-before-the-first-line-in-step-2-so-that-the-assignment-is-performed-only-once-then-set-the-stayinsync-property-to-true-so-that-rsttitleauthor-will-implicitly-and-automatically-change-to-the-corresponding-chapter-whenever-rst-moves-to-a-new-row"></a>[StayInSync](stayinsync-property-ado.md) プロパティが説明のために FALSE に設定されているので、外側ループのそれぞれの繰り返しの中で、明示的なチャプターの変化を確認できます。 ただし、手順 2 にある最初の行の前に手順 3 の割り当て作業を移動すると、割り当てが 1 回だけで済むので、より効率的になります。 **StayInSync**プロパティ TRUE に設定、*最初*は暗黙的に、自動的に変更に対応する章*rst*が新しい行に移動したときにできるようにします。)
=======
1. authors および titleauthor テーブルの **Recordset** オブジェクトが、author ID によって関連付けられます。

2. 外側のループで、各作成者の姓名、州、および ID が表示されます。

3. 各行に対して追加された **Recordset** が **Fields** コレクションから取得され、*rstTitleAuthor* に割り当てられます。

4. 内側のループで、追加された **Recordset** の各行からの 4 つのフィールドが表示されます。

> [!NOTE] 
> [StayInSync](stayinsync-property-ado.md)プロパティは、明示的に変更するには外側のループの各イテレーションでこの章を確認するための説明のため、FALSE に設定されます。 ただし、手順 2 にある最初の行の前に手順 3 の割り当て作業を移動すると、割り当てが 1 回だけで済むので、より効率的になります。 *最初*は暗黙的に、自動的に変更する対応する章を*rst*が新しい行に移動したときに**StayInSync**プロパティを true に設定します。
>>>>>>> master

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

