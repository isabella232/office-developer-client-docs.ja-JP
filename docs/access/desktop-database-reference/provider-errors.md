---
title: プロバイダー エラー (Access デスクトップ データベースリファレンス)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 4d2610be0ab206e5bb365b1147e06444ce7bbec7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59606409"
---
# <a name="provider-errors"></a>プロバイダー エラー


**適用先**: Access 2013、Office 2013 

プロバイダー エラーが発生すると、実行時エラー -2147467259 が返されます。このエラーを受け取った場合は、アクティブな **Connection** オブジェクトの、処理の内容を表す 1 つ以上のエラーが含まれる **Errors** コレクションを調べます。

## <a name="the-ado-errors-collection"></a>ADO Errors コレクション

特定の ADO 操作により複数のプロバイダー エラーが発生する可能性があるため、ADO では、 **Connection** オブジェクト経由でエラー オブジェクトのコレクションを公開しています。操作が正常に完了した場合、このコレクションにはオブジェクトは格納されず、なんらかの問題が生じ、プロバイダーで 1 つ以上のエラーが発生した場合は、このコレクションに 1 つ以上の **Error** オブジェクトが格納されます。エラーの正確な原因を突き止めるには、各エラー オブジェクトを個別に調べる必要があります。

発生したエラーの処理が完了したら、 **Clear** メソッドを呼び出してコレクションの内容を消去できます。 **Recordset** オブジェクトの **Resync** 、 **UpdateBatch** 、または **CancelBatch** の各メソッドの呼び出し、 **Connection** オブジェクトの **Open** メソッドの呼び出し、あるいは **Recordset** オブジェクトの **Filter** プロパティの設定を行う前に、 **Errors** コレクションの内容を明示的に消去することは特に重要です。コレクションを明示的に消去することで、以前の操作による **Error** オブジェクトがコレクションに残っていないことを確認できます。

エラー以外に警告を生成する操作もあります。警告も、 **Error** コレクションの **Errors** オブジェクトによって表されます。プロバイダーが警告をコレクションに追加する場合は、実行時エラーは生成されません。特定の操作によって警告が生成されたかどうかを確認するには、 **Errors** コレクションの **Count** プロパティを調べます。カウントが 1 以上の場合、 **Error** オブジェクトがコレクションに追加されています。 **Errors** コレクションにエラーまたは警告が含まれていることを判別した場合、コレクション内で反復処理を行って、各 **Error** オブジェクトの情報を取得できます。次の簡潔な Visual Basic のコード例にこの方法を示します。

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

エラー処理ルーチンでは、 **For Each** ループで **Errors** コレクション内の各オブジェクトを調べます。この例では、単に表示用のメッセージを蓄積しています。実際のプログラムでは、開いているすべてのファイルを閉じ、プログラムを正しい順序で停止するなど、各エラーに合わせて適切なタスクを実行するコードを記述します。

## <a name="the-error-object"></a>Error オブジェクト

**Error** オブジェクトを調べると、発生したエラーの種類を特定し、さらにエラーの原因になったアプリケーションまたはオブジェクトを特定できます。**Error** オブジェクトのプロパティは、次のとおりです。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>プロパティ名</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>説明</strong></p></td>
<td><p>発生したエラーを説明するテキストです。</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext, HelpFile</strong></p></td>
<td><p>発生したエラーの説明を含むヘルプ トピックとヘルプ ファイルを示します。</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>プロバイダー固有のエラー番号です。</p></td>
</tr>
<tr class="even">
<td><p><strong>数値</strong></p></td>
<td><p>発生したエラーに対応する <strong>ErrorValueEnum</strong> の番号を表す長整数です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>エラーが生じたオブジェクトまたはアプリケーションの名前を示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>プロバイダーが SQL ステートメントの処理中に返す 5 桁のエラー コードです。</p></td>
</tr>
</tbody>
</table>


ADO **Error** オブジェクトは、標準の Visual Basic **Err** オブジェクトによく似ています。発生したエラーの情報は、プロパティによって表されます。エラーの番号以外に、2 種類の関連情報も返されます。**NativeError** プロパティには、使用しているプロバイダーに固有のエラー番号が格納されます。前の例では、プロバイダーは Microsoft OLE DB Provider for SQL Server であるため、**NativeError** には SQL Server に固有のエラーが格納されます。**SQLState** プロパティには、SQL ステートメント内のエラーを示す 5 桁のコードが設定されます。

## <a name="event-related-errors"></a>イベント関連エラー

**Error** オブジェクトは、イベント関連エラーが発生した場合にも使用されます。イベント パラメーターとして渡される **Error** オブジェクトを調べることで、ADO イベントを発生させたプロセスでエラーが発生したかどうかを判断できます。

イベントを発生させた操作が正常に終了すると、イベント ハンドラーの *adStatus* パラメーターが *adStatusOK* に設定されます。一方、イベントを発生させた操作が失敗すると、*adStatus* パラメーターは *adStatusErrorsOccurred* に設定されます。この場合は、エラーを表す **Error** オブジェクトが *pError* パラメーターに格納されます。

