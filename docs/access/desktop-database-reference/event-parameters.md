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
# <a name="event-parameters"></a>イベント パラメーター

**適用先:** Access 2013、Office 2013

すべてのイベント ハンドラーには、イベント ハンドラーを制御するステータス パラメーターがあります。Complete イベントの場合、このパラメーターは、そのイベントを生成した操作の成功または失敗をも示します。また、ほとんどの Complete イベントには、その操作の実行に使用された ADO オブジェクトを参照する 1 つまたは複数のオブジェクト パラメーターに加えて、発生した可能性のあるエラーについての情報が設定されるエラー パラメーターもあります。たとえば、[ExecuteComplete](executecomplete-event-ado.md) イベントには、このイベントに関連する **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクト用のオブジェクト パラメーターが含まれています。次の Microsoft Visual Basic の例にある、pCommand オブジェクト、pRecordset オブジェクトと pConnection オブジェクトはそれぞれ、 **Execute** メソッドで使用される **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクトを表しています。

```vb 
 
Private Sub connEvent_ExecuteComplete(ByVal RecordsAffected As Long, _ 
 ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pCommand As ADODB.Command, _ 
 ByVal pRecordset As ADODB.Recordset, _ 
 ByVal pConnection As ADODB.Connection) 
```

**Error** オブジェクトを除いて、Will イベントには同じパラメーター群が渡されます。これにより、アプリケーションでは、保留中の操作に使用されている各オブジェクトを調べ、その操作の完了を許可するかどうかを決定することができます。

一部のイベントハンドラーには、イベントが発生した理由に関する追加情報を提供する*Reason*パラメーターがあります。 たとえば、 **MoveComplete**イベント**** は、1つのナビゲーションメソッド (**MoveNext**、 **MovePrevious**など) が呼び出されたとき、または再クエリの結果として発生することがあります。

## <a name="status-parameter"></a>ステータス パラメーター

イベント ハンドラー ルーチンが呼び出されると、"ステータス" パラメーターが次の値のいずれか 1 つに設定されます。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusOK</strong></p></td>
<td><p>Will イベントと Complete イベントの両方に渡されます。 イベントを発生させた操作が正常に完了したことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>Complete イベントにのみ渡されます。イベントを発生した操作が失敗したこと、または Will イベントがその操作をキャンセルしたことを示します。詳細については、「エラー パラメーター」を参照してください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Will イベントにのみ渡されます。 Will イベントで操作をキャンセルできないことを示します。 この操作は実行する必要があります。</p></td>
</tr>
</tbody>
</table>


この操作を続行する必要があるかどうかを判断する場合は、 *Status*パラメーターを変更しないでおきます。 ただし、受信状態パラメーターが**adstatuscantdeny**に設定されていない限り、*状態*を**adstatuscancel**に変更することで、保留中の操作を取り消すことができます。 これを行うと、操作に関連付けられている完全なイベントの*Status*パラメーターが**adstatuserrorソケット curred**に設定されます。 The **Error** object passed to the Complete event will contain the value **adErrOperationCancelled**.

イベントを処理する必要がなくなった場合は、 *Status*を**adStatusUnwantedEvent**に設定すると、アプリケーションでそのイベントの通知を受け取ることがなくなります。 Remember, however, that some events can be raised for more than one reason. In that case, you must specify **adStatusUnwantedEvent** for each possible reason. たとえば、保留中の**recordchange**イベントの通知を受信しないようにするためには、 *Status*パラメーターを**adrsnaddnew**、 **adrsnaddnew**、 **adrsnaddnew** **** **の adStatusUnwantedEvent に設定する必要があります。adRsnUndoUpdate**、 **adRsnUndoAddNew**、 **adRsnUndoDelete**、および**adrsnfirstchange**が発生したとき。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>値</p></th>
<th><p>説明</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adStatusUnwantedEvent</strong></p></td>
<td><p>イベント ハンドラーがこれ以降の通知を受け入れないようにします。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusCancel</strong></p></td>
<td><p>これから実行する操作のキャンセルを要求します。</p></td>
</tr>
</tbody>
</table>


## <a name="error-parameter"></a>エラー パラメーター

*error*パラメーターは、ADO [error](error-object-ado.md)オブジェクトへの参照です。 *Status*パラメーターが**adstatuserrorソケット curred**に設定されている場合、 **Error**オブジェクトには操作が失敗した理由に関する詳細が含まれています。 Complete イベントに関連付けられているイベントが、 *Status*パラメーターを**adstatuscancel**に設定することによって操作をキャンセルした場合、error オブジェクトは常に**adErrOperationCancelled**に設定されます。

## <a name="object-parameter"></a>オブジェクト パラメーター

各イベントでは、操作に関係するオブジェクトを表す 1 つまたは複数のオブジェクトを受け取ります。たとえば、**ExecuteComplete** イベントでは、**Command** オブジェクト、**Recordset** オブジェクト、および **Connection** オブジェクトを受け取ります。

## <a name="reason-parameter"></a>理由パラメーター

*Reason*パラメーター *adReason*は、イベントが発生した理由に関する追加情報を提供します。 *adReason*パラメーターを持つイベントは、同じ操作であっても、さまざまな理由で複数回呼び出されることがあります。 For example, the **WillChangeRecord** event handler is called for operations that are about to do or undo the insertion, deletion, or modification of a record. 特定の理由でイベントが発生した場合にのみイベントを処理する場合は、 *adReason*パラメーターを使用して、不要なオカレンスを除外することができます。 For example, if you wanted to process record-change events only when they occur because a record was added, you can do something like this:

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

この例では、処理対象外の理由それぞれに対して通知が発生する可能性があります。ただし、各理由に対して通知が発生するのは 1 回のみです。各理由に対して通知が 1 回発生した後には、新規レコード追加の場合にのみ通知を受け取ることになります。

これに対し、**adReason** パラメーターがないイベント ハンドラーでイベント通知を受け取らないように設定する場合は、*adStatus* を **adStatusUnwantedEvent** に 1 回設定するだけで済みます。

