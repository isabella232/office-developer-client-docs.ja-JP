---
title: 競合を検出し、解決する
TOCTitle: Detecting and Resolving Conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76bfc8f81b7f9df3d1b0e759620952f92bb5c8f1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875296"
---
# <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="8daca-102">競合を検出し、解決する</span><span class="sxs-lookup"><span data-stu-id="8daca-102">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="8daca-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8daca-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="detecting-and-resolving-conflicts"></a><span data-ttu-id="8daca-104">競合の検出および解決</span><span class="sxs-lookup"><span data-stu-id="8daca-104">Detecting and Resolving Conflicts</span></span>

<span data-ttu-id="8daca-p101">**Recordset** をイミディエイト モードで処理している場合は、同時操作の問題が発生する可能性はきわめて低いといえます。一方、アプリケーションでバッチ モードの更新を使用している場合は、あるユーザーがレコードに対して加えた変更が保存される前に、同じレコードを編集している他のユーザーがそのレコードを変更する可能性が十分にあります。このような場合、アプリケーションがその競合をスムーズに処理できると便利です。サーバーに最後に更新を送信した人が "勝者" となる方がよい場合もあれば、直近に更新を実行したユーザーに 2 つの競合する値を提示して、どちらの更新を採用するのか決定してもらう方がよい場合もあります。</span><span class="sxs-lookup"><span data-stu-id="8daca-p101">If you are dealing with your **Recordset** in immediate mode, there is much less chance for concurrency problems to arise. On the other hand, if your application uses batch mode updating, there may be a good chance that one user will change a record before changes made by another user editing the same record are saved. In such a case, you will want your application to gracefully handle the conflict. It may be your wish that the last person to send an update to the server "wins." Or you may want to let the most recent user to decide which update should take precedence by providing him with a choice between the two conflicting values.</span></span>

<span data-ttu-id="8daca-p102">いずれにしても、ADO では、この種類の競合を処理するために、 **Field** オブジェクトの **UnderlyingValue** プロパティと **OriginalValue** プロパティを使用します。これらのプロパティを **Recordset** の **Resync** メソッドおよび **Filter** プロパティと組み合わせて使用します。</span><span class="sxs-lookup"><span data-stu-id="8daca-p102">Whatever the case, ADO provides the **UnderlyingValue** and **OriginalValue** properties of the **Field** object in order to handle these types of conflicts. Use these properties in combination with the **Resync** method and **Filter** property of the **Recordset**.</span></span>

## <a name="detecting-errors"></a><span data-ttu-id="8daca-112">エラーを検出する</span><span class="sxs-lookup"><span data-stu-id="8daca-112">Detecting Errors</span></span>

<span data-ttu-id="8daca-p103">ADO がバッチ更新中に競合を検出すると、 **Errors** コレクションに警告が追加されます。このため、 **BatchUpdate** を呼び出した直後に、必ずエラーをチェックすることをお勧めします。エラーを発見したら、競合が発生したかどうかテストを開始します。まず、 **Recordset** の **Filter** プロパティを **adFilterConflictingRecords** に設定します ( **Filter** プロパティについては前の章で説明しています)。これにより、競合するレコードだけが **Recordset** に表示されます。この手順の後に **RecordCount** プロパティがゼロになっていれば、競合以外の原因でエラーが発生したことがわかります。</span><span class="sxs-lookup"><span data-stu-id="8daca-p103">When ADO encounters a conflict during a batch update, a warning will be placed in the **Errors** collection. Therefore, you should always check for errors immediately after calling **BatchUpdate**, and if you find them, begin testing the assumption that you have encountered a conflict. The first step is to set the **Filter** property on the **Recordset** equal to **adFilterConflictingRecords** (the **Filter** property is discussed in the preceding chapter). This limits the view on your **Recordset** to only those records that are in conflict. If the **RecordCount** property is equal to zero after this step, you know the error was raised by something other than a conflict.</span></span>

<span data-ttu-id="8daca-p104">**BatchUpdate** を呼び出すと、ADO およびプロバイダーは、データ ソースに対して更新を実行するための SQL ステートメントを生成します。一部のデータ ソースでは、WHERE 句で使用できる列の種類が限定されているため、注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="8daca-p104">When you call **BatchUpdate**, ADO and the provider are generating SQL statements to perform updates on the data source. Remember that certain data sources have limitations on which types of columns can be used in a WHERE clause.</span></span>

<span data-ttu-id="8daca-120">次に、 *AffectRecords*引数**adAffectGroup**に設定し、 *ResyncValues*引数を**処理**するのと同じ設定を**レコード セット**に**再同期**メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="8daca-120">Next, call the **Resync** method on the **Recordset** with the *AffectRecords* argument set equal to **adAffectGroup** and the *ResyncValues* argument set equal to **adResyncUnderlyingValues**.</span></span> <span data-ttu-id="8daca-121">**Resync**メソッドは、基になるデータベースから現在の**レコード セット**オブジェクト内のデータを更新します。</span><span class="sxs-lookup"><span data-stu-id="8daca-121">The **Resync** method refreshes the data in the current **Recordset** object from the underlying database.</span></span> <span data-ttu-id="8daca-122">**AdAffectGroup**を使用するは、データベースと現在のフィルターを設定するは、競合するレコードだけが表示されているレコードのみが再同期されることを確認します。</span><span class="sxs-lookup"><span data-stu-id="8daca-122">By using **adAffectGroup**, you are ensuring that only the records visible with the current filter setting, that is, only the conflicting records, are resynchronized with the database.</span></span> <span data-ttu-id="8daca-123">大きな**Recordset**を処理している場合は、パフォーマンスに大きな違いを作成このでした。</span><span class="sxs-lookup"><span data-stu-id="8daca-123">This could make a significant performance difference if you are dealing with a large **Recordset**.</span></span> <span data-ttu-id="8daca-124">**Resync**を呼び出すときに、**処理**に*ResyncValues*引数を設定することにより**UnderlyingValue**プロパティに、データベースから (競合) の値が含まれているがいることを確認する**値**値は、ユーザーが入力し、 **OriginalValue**プロパティが (最後の成功した**UpdateBatch**の呼び出しが行われた前に、の値) のフィールドの元の値を保持するプロパティが維持されます。</span><span class="sxs-lookup"><span data-stu-id="8daca-124">By setting the *ResyncValues* argument to **adResyncUnderlyingValues** when calling **Resync**, you ensure that the **UnderlyingValue** property will contain the (conflicting) value from the database, that the **Value** property will maintain the value entered by the user, and that the **OriginalValue** property will hold the original value for the field (the value it had before the last successful **UpdateBatch** call was made).</span></span> <span data-ttu-id="8daca-125">競合を解決するには、プログラムを使用してまたは使用する値を選択するユーザーを必要とするこれらの値を使用できます。</span><span class="sxs-lookup"><span data-stu-id="8daca-125">You can then use these values to resolve the conflict programmatically or require the user to choose the value that will be used.</span></span>

<span data-ttu-id="8daca-p106">この手法を次のコード例に示します。この例では、別の **Recordset** を使用して、 **UpdateBatch** が呼び出される前に基になるテーブルの値を変更することにより、意図的に競合を発生させます。</span><span class="sxs-lookup"><span data-stu-id="8daca-p106">This technique is shown in the code example below. The example artificially creates a conflict by using a separate **Recordset** to change a value in the underlying table before **UpdateBatch** is called.</span></span>

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

<span data-ttu-id="8daca-128">現在の **Record** または特定の **Field** の **Status** プロパティを使用すると、どのような競合が発生したのかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="8daca-128">You can use the **Status** property of the current **Record** or of a specific **Field** to determine what kind of a conflict has occurred.</span></span>

<span data-ttu-id="8daca-129">エラー処理の詳細については、「[6 章: エラー処理](chapter-6-error-handling.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8daca-129">For more detailed information on error handling, see [Chapter 6: Error Handling](chapter-6-error-handling.md).</span></span>

