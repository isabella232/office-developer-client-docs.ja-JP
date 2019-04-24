---
title: イベントパラメーター (Access デスクトップデータベースリファレンス)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd4a99ec24a05084a2ae137ded3219c2997f8cf3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293316"
---
# <a name="event-parameters"></a><span data-ttu-id="53243-102">イベント パラメーター</span><span class="sxs-lookup"><span data-stu-id="53243-102">Event parameters</span></span>

<span data-ttu-id="53243-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="53243-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="53243-p101">すべてのイベント ハンドラーには、イベント ハンドラーを制御するステータス パラメーターがあります。Complete イベントの場合、このパラメーターは、そのイベントを生成した操作の成功または失敗をも示します。また、ほとんどの Complete イベントには、その操作の実行に使用された ADO オブジェクトを参照する 1 つまたは複数のオブジェクト パラメーターに加えて、発生した可能性のあるエラーについての情報が設定されるエラー パラメーターもあります。たとえば、[ExecuteComplete](executecomplete-event-ado.md) イベントには、このイベントに関連する **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクト用のオブジェクト パラメーターが含まれています。次の Microsoft Visual Basic の例にある、pCommand オブジェクト、pRecordset オブジェクトと pConnection オブジェクトはそれぞれ、 **Execute** メソッドで使用される **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクトを表しています。</span><span class="sxs-lookup"><span data-stu-id="53243-p101">Every event handler has a status parameter that controls the event handler. For Complete events, this parameter is also used to indicate the success or failure of the operation that generated the event. Most Complete events also have an error parameter to provide information about any error that might have occurred, as well as one or more object parameters that refer to the ADO objects used to perform the operation. For example, the [ExecuteComplete](executecomplete-event-ado.md) event includes object parameters for the **Command**, **Recordset**, and **Connection** objects associated with the event. In the following Microsoft Visual Basic example, you can see the pCommand, pRecordset and pConnection objects which represent the **Command**, **Recordset**, and **Connection** objects used by the **Execute** method.</span></span>

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

<span data-ttu-id="53243-p102">**Error** オブジェクトを除いて、Will イベントには同じパラメーター群が渡されます。これにより、アプリケーションでは、保留中の操作に使用されている各オブジェクトを調べ、その操作の完了を許可するかどうかを決定することができます。</span><span class="sxs-lookup"><span data-stu-id="53243-p102">Except for the **Error** object, the same parameters are passed to the Will events. This gives you the opportunity to examine each of the objects to be used in the pending operation and determine whether the operation should be allowed to complete.</span></span>

<span data-ttu-id="53243-111">一部のイベントハンドラーには、イベントが発生した理由に関する追加情報を提供する*Reason*パラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="53243-111">Some event handlers have a *Reason* parameter, which provides additional information about why the event occurred.</span></span> <span data-ttu-id="53243-112">たとえば、 **MoveComplete**イベント\*\*\*\* は、1つのナビゲーションメソッド (**MoveNext**、 **MovePrevious**など) が呼び出されたとき、または再クエリの結果として発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="53243-112">For example, the **WillMove** and **MoveComplete** events can occur due to any one of the navigation methods (**MoveNext**, **MovePrevious**, and so on) being called or as the result of a requery.</span></span>

## <a name="status-parameter"></a><span data-ttu-id="53243-113">ステータス パラメーター</span><span class="sxs-lookup"><span data-stu-id="53243-113">Status Parameter</span></span>

<span data-ttu-id="53243-114">イベント ハンドラー ルーチンが呼び出されると、"ステータス" パラメーターが次の値のいずれか 1 つに設定されます。</span><span class="sxs-lookup"><span data-stu-id="53243-114">When the event-handler routine is called, the *Status* parameter is set to one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53243-115">値</span><span class="sxs-lookup"><span data-stu-id="53243-115">Value</span></span></p></th>
<th><p><span data-ttu-id="53243-116">説明</span><span class="sxs-lookup"><span data-stu-id="53243-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53243-117"><strong>adStatusOK</strong></span><span class="sxs-lookup"><span data-stu-id="53243-117"><strong>adStatusOK</strong></span></span></p></td>
<td><p><span data-ttu-id="53243-118">Will イベントと Complete イベントの両方に渡されます。</span><span class="sxs-lookup"><span data-stu-id="53243-118">Passed to both Will and Complete events.</span></span> <span data-ttu-id="53243-119">イベントを発生させた操作が正常に完了したことを示します。</span><span class="sxs-lookup"><span data-stu-id="53243-119">This value means that the operation that caused the event completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53243-120"><strong>adStatusErrorsOccurred</strong></span><span class="sxs-lookup"><span data-stu-id="53243-120"><strong>adStatusErrorsOccurred</strong></span></span></p></td>
<td><p><span data-ttu-id="53243-p105">Complete イベントにのみ渡されます。イベントを発生した操作が失敗したこと、または Will イベントがその操作をキャンセルしたことを示します。詳細については、「エラー パラメーター」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="53243-p105">Passed to Complete events only. This value means that the operation that caused the event was unsuccessful, or a Will event canceled the operation. Check the <em>Error</em> parameter for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="53243-124"><strong>adStatusCantDeny</strong></span><span class="sxs-lookup"><span data-stu-id="53243-124"><strong>adStatusCantDeny</strong></span></span></p></td>
<td><p><span data-ttu-id="53243-125">Will イベントにのみ渡されます。</span><span class="sxs-lookup"><span data-stu-id="53243-125">Passed to Will events only.</span></span> <span data-ttu-id="53243-126">Will イベントで操作をキャンセルできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="53243-126">This value means that the operation cannot be canceled by the Will event.</span></span> <span data-ttu-id="53243-127">この操作は実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="53243-127">It must be performed.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="53243-128">この操作を続行する必要があるかどうかを判断する場合は、 *Status*パラメーターを変更しないでおきます。</span><span class="sxs-lookup"><span data-stu-id="53243-128">If you determine in your Will event that the operation should continue, leave the *Status* parameter unchanged.</span></span> <span data-ttu-id="53243-129">ただし、受信状態パラメーターが**adstatuscantdeny**に設定されていない限り、*状態*を**adstatuscancel**に変更することで、保留中の操作を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="53243-129">As long as the incoming status parameter was not set to **adStatusCantDeny**, however, you can cancel the pending operation by changing *Status* to **adStatusCancel**.</span></span> <span data-ttu-id="53243-130">これを行うと、操作に関連付けられている完全なイベントの*Status*パラメーターが**adstatuserrorソケット curred**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="53243-130">When you do so, the Complete event associated with the operation has its *Status* parameter set to **adStatusErrorsOccurred**.</span></span> <span data-ttu-id="53243-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span><span class="sxs-lookup"><span data-stu-id="53243-131">The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.</span></span>

<span data-ttu-id="53243-132">イベントを処理する必要がなくなった場合は、 *Status*を**adStatusUnwantedEvent**に設定すると、アプリケーションでそのイベントの通知を受け取ることがなくなります。</span><span class="sxs-lookup"><span data-stu-id="53243-132">If you no longer want to process an event, you can set *Status* to **adStatusUnwantedEvent** and your application will no longer receive notification of that event.</span></span> <span data-ttu-id="53243-133">Remember, however, that some events can be raised for more than one reason.</span><span class="sxs-lookup"><span data-stu-id="53243-133">Remember, however, that some events can be raised for more than one reason.</span></span> <span data-ttu-id="53243-134">In that case, you must specify **adStatusUnwantedEvent** for each possible reason.</span><span class="sxs-lookup"><span data-stu-id="53243-134">In that case, you must specify **adStatusUnwantedEvent** for each possible reason.</span></span> <span data-ttu-id="53243-135">たとえば、保留中の**recordchange**イベントの通知を受信しないようにするためには、 *Status*パラメーターを**adrsnaddnew**、 **adrsnaddnew**、 **adrsnaddnew** \*\*\*\* **の adStatusUnwantedEvent に設定する必要があります。adRsnUndoUpdate**、 **adRsnUndoAddNew**、 **adRsnUndoDelete**、および**adrsnfirstchange**が発生したとき。</span><span class="sxs-lookup"><span data-stu-id="53243-135">For example, in order to stop receiving notification of pending **RecordChange** events, you must set the *Status* parameter to **adStatusUnwantedEvent** for **adRsnAddNew**, **adRsnDelete**, **adRsnUpdate**, **adRsnUndoUpdate**, **adRsnUndoAddNew**, **adRsnUndoDelete**, and **adRsnFirstChange** as they occur.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="53243-136">値</span><span class="sxs-lookup"><span data-stu-id="53243-136">Value</span></span></p></th>
<th><p><span data-ttu-id="53243-137">説明</span><span class="sxs-lookup"><span data-stu-id="53243-137">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="53243-138"><strong>adStatusUnwantedEvent</strong></span><span class="sxs-lookup"><span data-stu-id="53243-138"><strong>adStatusUnwantedEvent</strong></span></span></p></td>
<td><p><span data-ttu-id="53243-139">イベント ハンドラーがこれ以降の通知を受け入れないようにします。</span><span class="sxs-lookup"><span data-stu-id="53243-139">Request that this event handler receive no further notifications.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="53243-140"><strong>adStatusCancel</strong></span><span class="sxs-lookup"><span data-stu-id="53243-140"><strong>adStatusCancel</strong></span></span></p></td>
<td><p><span data-ttu-id="53243-141">これから実行する操作のキャンセルを要求します。</span><span class="sxs-lookup"><span data-stu-id="53243-141">Request cancellation of the operation that is about to occur.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a><span data-ttu-id="53243-142">エラー パラメーター</span><span class="sxs-lookup"><span data-stu-id="53243-142">Error Parameter</span></span>

<span data-ttu-id="53243-143">*error*パラメーターは、ADO [error](error-object-ado.md)オブジェクトへの参照です。</span><span class="sxs-lookup"><span data-stu-id="53243-143">The *Error* parameter is a reference to an ADO [Error](error-object-ado.md) object.</span></span> <span data-ttu-id="53243-144">*Status*パラメーターが**adstatuserrorソケット curred**に設定されている場合、 **Error**オブジェクトには操作が失敗した理由に関する詳細が含まれています。</span><span class="sxs-lookup"><span data-stu-id="53243-144">When the *Status* parameter is set to **adStatusErrorsOccurred**, the **Error** object contains details about why the operation failed.</span></span> <span data-ttu-id="53243-145">Complete イベントに関連付けられているイベントが、 *Status*パラメーターを**adstatuscancel**に設定することによって操作をキャンセルした場合、error オブジェクトは常に**adErrOperationCancelled**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="53243-145">If the Will event associated with a Complete event has canceled the operation by setting the *Status* parameter to **adStatusCancel**, the error object is always set to **adErrOperationCancelled**.</span></span>

## <a name="object-parameter"></a><span data-ttu-id="53243-146">オブジェクト パラメーター</span><span class="sxs-lookup"><span data-stu-id="53243-146">Object Parameter</span></span>

<span data-ttu-id="53243-p110">各イベントでは、操作に関係するオブジェクトを表す 1 つまたは複数のオブジェクトを受け取ります。たとえば、**ExecuteComplete** イベントでは、**Command** オブジェクト、**Recordset** オブジェクト、および **Connection** オブジェクトを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="53243-p110">Each event receives one or more objects representing the objects that are involved in the operation. For example, the **ExecuteComplete** event receives a **Command** object, a **Recordset** object, and a **Connection** object.</span></span>

## <a name="reason-parameter"></a><span data-ttu-id="53243-149">理由パラメーター</span><span class="sxs-lookup"><span data-stu-id="53243-149">Reason Parameter</span></span>

<span data-ttu-id="53243-150">*Reason*パラメーター *adReason*は、イベントが発生した理由に関する追加情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="53243-150">The *Reason* parameter, *adReason*, provides additional information about why the event occurred.</span></span> <span data-ttu-id="53243-151">*adReason*パラメーターを持つイベントは、同じ操作であっても、さまざまな理由で複数回呼び出されることがあります。</span><span class="sxs-lookup"><span data-stu-id="53243-151">Events with an *adReason* parameter may be called several times, even for the same operation, each time for a different reason.</span></span> <span data-ttu-id="53243-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span><span class="sxs-lookup"><span data-stu-id="53243-152">For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record.</span></span> <span data-ttu-id="53243-153">特定の理由でイベントが発生した場合にのみイベントを処理する場合は、 *adReason*パラメーターを使用して、不要なオカレンスを除外することができます。</span><span class="sxs-lookup"><span data-stu-id="53243-153">If you want to process an event only when it occurs for a particular reason, you can use the *adReason* parameter to filter out the occurrences you are not interested in.</span></span> <span data-ttu-id="53243-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span><span class="sxs-lookup"><span data-stu-id="53243-154">For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:</span></span>

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

<span data-ttu-id="53243-p112">この例では、処理対象外の理由それぞれに対して通知が発生する可能性があります。ただし、各理由に対して通知が発生するのは 1 回のみです。各理由に対して通知が 1 回発生した後には、新規レコード追加の場合にのみ通知を受け取ることになります。</span><span class="sxs-lookup"><span data-stu-id="53243-p112">In this case, notification can potentially occur for each of the other reasons. However, it will occur only once for each reason. After the notification has occurred once for each reason, you will receive notification only for the addition of a new record.</span></span>

<span data-ttu-id="53243-158">これに対し、**adReason** パラメーターがないイベント ハンドラーでイベント通知を受け取らないように設定する場合は、*adStatus* を **adStatusUnwantedEvent** に 1 回設定するだけで済みます。</span><span class="sxs-lookup"><span data-stu-id="53243-158">In contrast, you need to set *adStatus* to **adStatusUnwantedEvent** only one time to request that an event handler without an **adReason** parameter stop receiving event notifications.</span></span>

