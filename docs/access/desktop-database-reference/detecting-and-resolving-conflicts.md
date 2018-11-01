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
# <a name="detecting-and-resolving-conflicts"></a>競合を検出し、解決する

**適用されます**Access 2013、Office 2013。

## <a name="detecting-and-resolving-conflicts"></a>競合の検出および解決

**Recordset** をイミディエイト モードで処理している場合は、同時操作の問題が発生する可能性はきわめて低いといえます。一方、アプリケーションでバッチ モードの更新を使用している場合は、あるユーザーがレコードに対して加えた変更が保存される前に、同じレコードを編集している他のユーザーがそのレコードを変更する可能性が十分にあります。このような場合、アプリケーションがその競合をスムーズに処理できると便利です。サーバーに最後に更新を送信した人が "勝者" となる方がよい場合もあれば、直近に更新を実行したユーザーに 2 つの競合する値を提示して、どちらの更新を採用するのか決定してもらう方がよい場合もあります。

いずれにしても、ADO では、この種類の競合を処理するために、 **Field** オブジェクトの **UnderlyingValue** プロパティと **OriginalValue** プロパティを使用します。これらのプロパティを **Recordset** の **Resync** メソッドおよび **Filter** プロパティと組み合わせて使用します。

## <a name="detecting-errors"></a>エラーを検出する

ADO がバッチ更新中に競合を検出すると、 **Errors** コレクションに警告が追加されます。このため、 **BatchUpdate** を呼び出した直後に、必ずエラーをチェックすることをお勧めします。エラーを発見したら、競合が発生したかどうかテストを開始します。まず、 **Recordset** の **Filter** プロパティを **adFilterConflictingRecords** に設定します ( **Filter** プロパティについては前の章で説明しています)。これにより、競合するレコードだけが **Recordset** に表示されます。この手順の後に **RecordCount** プロパティがゼロになっていれば、競合以外の原因でエラーが発生したことがわかります。

**BatchUpdate** を呼び出すと、ADO およびプロバイダーは、データ ソースに対して更新を実行するための SQL ステートメントを生成します。一部のデータ ソースでは、WHERE 句で使用できる列の種類が限定されているため、注意が必要です。

次に、 *AffectRecords*引数**adAffectGroup**に設定し、 *ResyncValues*引数を**処理**するのと同じ設定を**レコード セット**に**再同期**メソッドを呼び出します。 **Resync**メソッドは、基になるデータベースから現在の**レコード セット**オブジェクト内のデータを更新します。 **AdAffectGroup**を使用するは、データベースと現在のフィルターを設定するは、競合するレコードだけが表示されているレコードのみが再同期されることを確認します。 大きな**Recordset**を処理している場合は、パフォーマンスに大きな違いを作成このでした。 **Resync**を呼び出すときに、**処理**に*ResyncValues*引数を設定することにより**UnderlyingValue**プロパティに、データベースから (競合) の値が含まれているがいることを確認する**値**値は、ユーザーが入力し、 **OriginalValue**プロパティが (最後の成功した**UpdateBatch**の呼び出しが行われた前に、の値) のフィールドの元の値を保持するプロパティが維持されます。 競合を解決するには、プログラムを使用してまたは使用する値を選択するユーザーを必要とするこれらの値を使用できます。

この手法を次のコード例に示します。この例では、別の **Recordset** を使用して、 **UpdateBatch** が呼び出される前に基になるテーブルの値を変更することにより、意図的に競合を発生させます。

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

現在の **Record** または特定の **Field** の **Status** プロパティを使用すると、どのような競合が発生したのかを判断できます。

エラー処理の詳細については、「[6 章: エラー処理](chapter-6-error-handling.md)」を参照してください。

