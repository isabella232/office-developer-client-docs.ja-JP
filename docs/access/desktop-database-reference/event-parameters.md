---
title: イベントのパラメーター (デスクトップ データベース参照のアクセス)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3acad111c3e1329f50c64f3f6fd6c5f7430e558d
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946742"
---
# <a name="event-parameters"></a><span data-ttu-id="8514d-102">イベント パラメーター</span><span class="sxs-lookup"><span data-stu-id="8514d-102">Event parameters</span></span>

<span data-ttu-id="8514d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="8514d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8514d-p101">すべてのイベント ハンドラーには、イベント ハンドラーを制御するステータス パラメーターがあります。Complete イベントの場合、このパラメーターは、そのイベントを生成した操作の成功または失敗をも示します。また、ほとんどの Complete イベントには、その操作の実行に使用された ADO オブジェクトを参照する 1 つまたは複数のオブジェクト パラメーターに加えて、発生した可能性のあるエラーについての情報が設定されるエラー パラメーターもあります。たとえば、[ExecuteComplete](executecomplete-event-ado.md) イベントには、このイベントに関連する **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクト用のオブジェクト パラメーターが含まれています。次の Microsoft Visual Basic の例にある、pCommand オブジェクト、pRecordset オブジェクトと pConnection オブジェクトはそれぞれ、 **Execute** メソッドで使用される **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクトを表しています。</span><span class="sxs-lookup"><span data-stu-id="8514d-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="8514d-p102">**Error** オブジェクトを除いて、Will イベントには同じパラメーター群が渡されます。これにより、アプリケーションでは、保留中の操作に使用されている各オブジェクトを調べ、その操作の完了を許可するかどうかを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="8514d-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="8514d-111">いくつかのイベント ハンドラーでは、イベントが発生した原因に関する追加情報を提供する*ため*のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="8514d-111">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred.</span></span> <span data-ttu-id="8514d-112">(**MoveNext**、 **MovePrevious**というように) は、ナビゲーション メソッドのいずれかが発生したため、 **WillMove**イベントと**MoveComplete**イベントを発生することがなどが呼び出された、または、再クエリの結果として。</span><span class="sxs-lookup"><span data-stu-id="8514d-112">For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="8514d-113">ステータス パラメーター</span><span class="sxs-lookup"><span data-stu-id="8514d-113">Status Parameter</span></span>

<span data-ttu-id="8514d-114">イベント ハンドラー ルーチンが呼び出されると、*状態*のパラメーターは次の値のいずれかに設定されています。</span><span class="sxs-lookup"><span data-stu-id="8514d-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8514d-115">値</span><span class="sxs-lookup"><span data-stu-id="8514d-115">Value</span></span></p></th>
<th><p><span data-ttu-id="8514d-116">説明</span><span class="sxs-lookup"><span data-stu-id="8514d-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8514d-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="8514d-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="8514d-p104">Will イベントと Complete イベントの両方に渡されます。イベントを発生させた操作が正常に完了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="8514d-p104">Passed to both Will and Complete events. This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8514d-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="8514d-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="8514d-121">完全なイベントのみに渡されます。</span><span class="sxs-lookup"><span data-stu-id="8514d-121">Passed to Complete events only.</span></span> <span data-ttu-id="8514d-122">この場合、イベントを発生させた操作が成功すると、できなかったこと、または Will イベントで操作がキャンセルされました。</span><span class="sxs-lookup"><span data-stu-id="8514d-122">This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation.</span></span> <span data-ttu-id="8514d-123">詳細については、「<em>エラー</em>パラメーターを確認していますください。</span><span class="sxs-lookup"><span data-stu-id="8514d-123">Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8514d-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="8514d-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="8514d-p106">Will イベントにのみ渡されます。Will イベントで操作をキャンセルできないことを示します。この操作は実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8514d-p106">Passed to Will events only. This value means that the operation cannot be canceled by the Will event. It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8514d-128">判断した場合、操作を続行する必要がありますがイベントで、変更されていない*状態*のパラメーターのままにします。</span><span class="sxs-lookup"><span data-stu-id="8514d-128">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged.</span></span> <span data-ttu-id="8514d-129">受信状態のパラメーターが**adStatusCantDeny**に設定されていない限り、ただし、*ステータス*を**adStatusCancel**に変更することで、保留中の操作をキャンセルできます。</span><span class="sxs-lookup"><span data-stu-id="8514d-129">As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**.</span></span> <span data-ttu-id="8514d-130">これを行うには、操作に関連付けられている完全なイベントは**adStatusErrorsOccurred**に設定されて、*ステータス*パラメーターを持ちます。</span><span class="sxs-lookup"><span data-stu-id="8514d-130">When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**.</span></span> <span data-ttu-id="8514d-131">Complete イベントに渡される**Error**オブジェクトには、 **adErrOperationCancelled**の値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8514d-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="8514d-132">イベントを処理しない場合は、*状態*を**adStatusUnwantedEvent**に設定して、アプリケーションでは、そのイベントの通知は送信されなくなります。</span><span class="sxs-lookup"><span data-stu-id="8514d-132">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event.</span></span> <span data-ttu-id="8514d-133">ただし、理由の 1 つ以上のいくつかのイベントが発生することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8514d-133">Remember, however, that some events can be raised for more than one reason.</span></span> <span data-ttu-id="8514d-134">その場合は、可能な各理由に対して**adStatusUnwantedEvent**を指定してください。</span><span class="sxs-lookup"><span data-stu-id="8514d-134">In that case, you must specify **adStatusUnwantedEvent** for each possible reason.</span></span> <span data-ttu-id="8514d-135">たとえば、保留中の**RecordChange**イベントの通知の受信を停止するために必要がありますパラメーターを設定する、*状態* **adRsnAddNew**、 **adRsnDelete**、 **adRsnUpdate\*\*\*\*を**adStatusUnwantedEvent**にadRsnUndoUpdate**、 **adRsnUndoAddNew**、 **adRsnUndoDelete**、および発生するときに、その**adRsnFirstChange**です。</span><span class="sxs-lookup"><span data-stu-id="8514d-135">For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8514d-136">値</span><span class="sxs-lookup"><span data-stu-id="8514d-136">Value</span></span></p></th>
<th><p><span data-ttu-id="8514d-137">説明</span><span class="sxs-lookup"><span data-stu-id="8514d-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8514d-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="8514d-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="8514d-139">イベント ハンドラーがこれ以降の通知を受け入れないようにします。</span><span class="sxs-lookup"><span data-stu-id="8514d-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8514d-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="8514d-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="8514d-141">これから実行する操作のキャンセルを要求します。</span><span class="sxs-lookup"><span data-stu-id="8514d-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="8514d-142">エラー パラメーター</span><span class="sxs-lookup"><span data-stu-id="8514d-142">Error Parameter</span></span>

<span data-ttu-id="8514d-143">*エラー*のパラメーターは、[エラー](error-object-ado.md)の ADO オブジェクトへの参照です。</span><span class="sxs-lookup"><span data-stu-id="8514d-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="8514d-144">*状態*パラメーターは、 **adStatusErrorsOccurred**に設定されている場合、 **Error**オブジェクトには、操作が失敗した理由に関する詳細情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8514d-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="8514d-145">Complete イベントに関連付けられた Will イベントは、*状態*のパラメーターを**adStatusCancel**に設定することにより操作がキャンセルされましたが場合、エラー オブジェクトは常に**adErrOperationCancelled**に設定します。</span><span class="sxs-lookup"><span data-stu-id="8514d-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="8514d-146">オブジェクト パラメーター</span><span class="sxs-lookup"><span data-stu-id="8514d-146">Object Parameter</span></span>

<span data-ttu-id="8514d-p110">各イベントでは、操作に関係するオブジェクトを表す 1 つまたは複数のオブジェクトを受け取ります。たとえば、 **ExecuteComplete** イベントでは、 **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクトを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="8514d-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="8514d-149">理由パラメーター</span><span class="sxs-lookup"><span data-stu-id="8514d-149">Reason Parameter</span></span>

<span data-ttu-id="8514d-150">*"理由*"パラメーター *adReason*は、イベントが発生した原因に関する追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="8514d-150">The *Reason* parameter, *adReason*, provides additional information about why the event occurred.</span></span> <span data-ttu-id="8514d-151">*AdReason*パラメーターを持つイベントは、別の理由で毎回、同じ操作の場合でも何回か呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8514d-151">Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason.</span></span> <span data-ttu-id="8514d-152">たとえば、 **WillChangeRecord**イベントのハンドラーは、しようとしたりしないで、挿入、削除、またはレコードの変更を元に戻す操作に対して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8514d-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span></span> <span data-ttu-id="8514d-153">何らかの理由で発生したときにのみイベントを処理する場合に興味はないフィルターをかけて、 *adReason*パラメーターを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="8514d-153">If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in.</span></span> <span data-ttu-id="8514d-154">たとえば、レコードが追加されたために発生したときにのみ、レコードの変更イベントを処理する場合は、行うことができます次のような何か。</span><span class="sxs-lookup"><span data-stu-id="8514d-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

```vb 
 
' BeginEventExampleVB01 
Private Sub rsTest_WillChangeRecord(ByVal adReason As ADODB.EventReasonEnum, ByVal cRecords As Long, adStatus As ADODB.EventStatusEnum, ByVal pRecordset As ADODB.Recordset) 
 If adReason = adRsnAddNew Then 
 ' Process event 
 '... 
 Else 
 ' Cancel event notification for all 
 ' other possible adReason values. 
 adStatus = adStatusUnwantedEvent 
 End If 
End Sub 
' EndEventExampleVB01 
```

<span data-ttu-id="8514d-p112">この例では、処理対象外の理由それぞれに対して通知が発生する可能性があります。ただし、各理由に対して通知が発生するのは 1 回のみです。各理由に対して通知が 1 回発生した後には、新規レコード追加の場合にのみ通知を受け取ることになります。</span><span class="sxs-lookup"><span data-stu-id="8514d-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="8514d-158">一方、 *adStatus* **adStatusUnwantedEvent**を 1 回だけを要求するイベント ハンドラーを設定せず、 **adReason**パラメーター停止イベントの通知を受信する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8514d-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

