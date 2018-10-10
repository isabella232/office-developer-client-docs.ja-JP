---
title: プロバイダー エラー (アクセス デスクトップ データベース参照)
TOCTitle: Provider Errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74d5381298f58c00c66ee4fb72504ce44f5dd7b5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25478902"
---
# <a name="provider-errors"></a><span data-ttu-id="32fee-102">プロバイダー エラー</span><span class="sxs-lookup"><span data-stu-id="32fee-102">Provider Errors</span></span>


<span data-ttu-id="32fee-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="32fee-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="32fee-p101">プロバイダー エラーが発生すると、実行時エラー -2147467259 が返されます。このエラーを受け取った場合は、アクティブな **Connection** オブジェクトの、処理の内容を表す 1 つ以上のエラーが含まれる **Errors** コレクションを調べます。</span><span class="sxs-lookup"><span data-stu-id="32fee-p101">When a provider error occurs, a run-time error of -2147467259 is returned. When you receive this error, check the active **Connection** object's **Errors** collection, which will contain one or more errors describing what happened.</span></span>

## <a name="the-ado-errors-collection"></a><span data-ttu-id="32fee-106">ADO Errors コレクション</span><span class="sxs-lookup"><span data-stu-id="32fee-106">The ADO Errors Collection</span></span>

<span data-ttu-id="32fee-p102">特定の ADO 操作により複数のプロバイダー エラーが発生する可能性があるため、ADO では、 **Connection** オブジェクト経由でエラー オブジェクトのコレクションを公開しています。操作が正常に完了した場合、このコレクションにはオブジェクトは格納されず、なんらかの問題が生じ、プロバイダーで 1 つ以上のエラーが発生した場合は、このコレクションに 1 つ以上の **Error** オブジェクトが格納されます。エラーの正確な原因を突き止めるには、各エラー オブジェクトを個別に調べる必要があります。</span><span class="sxs-lookup"><span data-stu-id="32fee-p102">Because a particular ADO operation can produce multiple provider errors, ADO exposes a collection of error objects through the **Connection** object. This collection contains no objects if an operation concludes successfully and contains one or more **Error** objects if something went wrong and the provider raised one or more errors. Examine each individual error object in order to determine the exact cause of the error.</span></span>

<span data-ttu-id="32fee-p103">発生したエラーの処理が完了したら、 **Clear** メソッドを呼び出してコレクションの内容を消去できます。 **Recordset** オブジェクトの **Resync** 、 **UpdateBatch** 、または **CancelBatch** の各メソッドの呼び出し、 **Connection** オブジェクトの **Open** メソッドの呼び出し、あるいは **Recordset** オブジェクトの **Filter** プロパティの設定を行う前に、 **Errors** コレクションの内容を明示的に消去することは特に重要です。コレクションを明示的に消去することで、以前の操作による **Error** オブジェクトがコレクションに残っていないことを確認できます。</span><span class="sxs-lookup"><span data-stu-id="32fee-p103">Once you have finished handling any errors that have occurred, you can clear the collection by calling the **Clear** method. It is particularly important to explicitly clear the **Errors** collection before you call the **Resync**, **UpdateBatch**, or **CancelBatch** method on a **Recordset** object, the **Open** method on a **Connection** object, or set the **Filter** property on a **Recordset** object. By clearing the collection explicitly, you can be certain that any **Error** objects in the collection are not left over from a previous operation.</span></span>

<span data-ttu-id="32fee-p104">エラー以外に警告を生成する操作もあります。警告も、 **Error** コレクションの **Errors** オブジェクトによって表されます。プロバイダーが警告をコレクションに追加する場合は、実行時エラーは生成されません。特定の操作によって警告が生成されたかどうかを確認するには、 **Errors** コレクションの **Count** プロパティを調べます。カウントが 1 以上の場合、 **Error** オブジェクトがコレクションに追加されています。 **Errors** コレクションにエラーまたは警告が含まれていることを判別した場合、コレクション内で反復処理を行って、各 **Error** オブジェクトの情報を取得できます。次の簡潔な Visual Basic のコード例にこの方法を示します。</span><span class="sxs-lookup"><span data-stu-id="32fee-p104">Some operations can generate warnings as well as errors. Warnings are also represented by **Error** objects in the **Errors** collection. When a provider adds a warning to the collection, it does not generate a run-time error. Check the **Count** property of the **Errors** collection to determine if a warning was produced by a particular operation. If the count is one or greater, an **Error** object has been added to the collection. Once you have determined that the **Errors** collection contains errors or warnings, you can iterate through the collection and retrieve information about each of the **Error** objects it contains. The following short Visual Basic example demonstrates this:</span></span>

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

<span data-ttu-id="32fee-p105">エラー処理ルーチンでは、 **For Each** ループで **Errors** コレクション内の各オブジェクトを調べます。この例では、単に表示用のメッセージを蓄積しています。実際のプログラムでは、開いているすべてのファイルを閉じ、プログラムを正しい順序で停止するなど、各エラーに合わせて適切なタスクを実行するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="32fee-p105">The error-handling routine includes a **For Each** loop that examines each object in the **Errors** collection. In this example, it simply accumulates a message for display. In a working program, you would write code to perform an appropriate task for each error, such as closing all open files and shutting down the program in an orderly fashion.</span></span>

## <a name="the-error-object"></a><span data-ttu-id="32fee-123">Error オブジェクト</span><span class="sxs-lookup"><span data-stu-id="32fee-123">The Error Object</span></span>

<span data-ttu-id="32fee-p106">**Error** オブジェクトを調べると、発生したエラーの種類を特定し、さらにエラーの原因になったアプリケーションまたはオブジェクトを特定できます。 **Error** オブジェクトのプロパティは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="32fee-p106">By examining an **Error** object you can determine what error occurred, and more importantly, what application or what object caused the error. The **Error** object has the following properties:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32fee-126">プロパティ名</span><span class="sxs-lookup"><span data-stu-id="32fee-126">Property name</span></span></p></th>
<th><p><span data-ttu-id="32fee-127">説明</span><span class="sxs-lookup"><span data-stu-id="32fee-127">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32fee-128"><strong>Description</strong></span><span class="sxs-lookup"><span data-stu-id="32fee-128"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="32fee-129">発生したエラーを説明するテキストです。</span><span class="sxs-lookup"><span data-stu-id="32fee-129">A text description of the error that occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32fee-130"><strong>HelpContext、HelpFile</strong></span><span class="sxs-lookup"><span data-stu-id="32fee-130"><strong>HelpContext, HelpFile</strong></span></span></p></td>
<td><p><span data-ttu-id="32fee-131">発生したエラーの説明を含むヘルプ トピックとヘルプ ファイルを示します。</span><span class="sxs-lookup"><span data-stu-id="32fee-131">Refers to the help topic and help file that contain a description of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32fee-132"><strong>以下</strong></span><span class="sxs-lookup"><span data-stu-id="32fee-132"><strong>NativeError</strong></span></span></p></td>
<td><p><span data-ttu-id="32fee-133">プロバイダー固有のエラー番号です。</span><span class="sxs-lookup"><span data-stu-id="32fee-133">The provider-specific error number.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32fee-134"><strong>番号</strong></span><span class="sxs-lookup"><span data-stu-id="32fee-134"><strong>Number</strong></span></span></p></td>
<td><p><span data-ttu-id="32fee-135">発生したエラーに対応する <strong>ErrorValueEnum</strong> の番号を表す長整数です。</span><span class="sxs-lookup"><span data-stu-id="32fee-135">A Long Integer that represents the number (listed in the <strong>ErrorValueEnum</strong>) of the error that occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32fee-136"><strong>Source</strong></span><span class="sxs-lookup"><span data-stu-id="32fee-136"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="32fee-137">エラーが生じたオブジェクトまたはアプリケーションの名前を示します。</span><span class="sxs-lookup"><span data-stu-id="32fee-137">Indicates the name of the object or application that generated an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32fee-138"><strong>SQLState</strong></span><span class="sxs-lookup"><span data-stu-id="32fee-138"><strong>SQLState</strong></span></span></p></td>
<td><p><span data-ttu-id="32fee-139">プロバイダーが SQL ステートメントの処理中に返す 5 桁のエラー コードです。</span><span class="sxs-lookup"><span data-stu-id="32fee-139">A five-character error code that the provider returns during the process of a SQL statement.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="32fee-p107">ADO **Error** オブジェクトは、標準の Visual Basic **Err** オブジェクトによく似ています。発生したエラーの情報は、プロパティによって表されます。エラーの番号以外に、2 種類の関連情報も返されます。 **NativeError** プロパティには、使用しているプロバイダーに固有のエラー番号が格納されます。前の例では、プロバイダーは Microsoft OLE DB Provider for SQL Server であるため、 **NativeError** には SQL Server に固有のエラーが格納されます。 **SQLState** プロパティには、SQL ステートメント内のエラーを示す 5 桁のコードが設定されます。</span><span class="sxs-lookup"><span data-stu-id="32fee-p107">The ADO **Error** object is quite similar to the standard Visual Basic **Err** object. Its properties describe the error that occurred. In addition to the number of the error, you also receive two related pieces of information. The **NativeError** property contains an error number specific to the provider you are using. In the previous example, the provider is the Microsoft OLE DB Provider for SQL Server, so **NativeError** will contain errors specific to SQL Server. The **SQLState** property has a five-letter code that describes an error in a SQL statement.</span></span>

## <a name="event-related-errors"></a><span data-ttu-id="32fee-146">イベント関連エラー</span><span class="sxs-lookup"><span data-stu-id="32fee-146">Event-Related Errors</span></span>

<span data-ttu-id="32fee-p108">**Error** オブジェクトは、イベント関連エラーが発生した場合にも使用されます。イベント パラメーターとして渡される **Error** オブジェクトを調べることで、ADO イベントを発生させたプロセスでエラーが発生したかどうかを判断できます。</span><span class="sxs-lookup"><span data-stu-id="32fee-p108">The **Error** object is also used when event-related errors occur. You can determine if an error occurred in the process that raised an ADO event by checking the **Error** object passed as an event parameter.</span></span>

<span data-ttu-id="32fee-p109">イベントを発生させた操作が正常に終了すると、イベント ハンドラーの *adStatus* パラメーターが *adStatusOK* に設定されます。一方、イベントを発生させた操作が失敗すると、*adStatus* パラメーターは *adStatusErrorsOccurred* に設定されます。この場合は、エラーを表す **Error** オブジェクトが *pError* パラメーターに格納されます。</span><span class="sxs-lookup"><span data-stu-id="32fee-p109">If the operation that causes an event is concluded successfully, the *adStatus* parameter of the event handler will be set to *adStatusOK*. On the other hand, if the operation that raised the event was unsuccessful, the *adStatus* parameter is set to *adStatusErrorsOccurred*. In that case, the *pError* parameter will contain an **Error** object that describes the error.</span></span>

