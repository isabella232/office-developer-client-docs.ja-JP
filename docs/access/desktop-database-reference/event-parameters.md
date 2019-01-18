---
title: イベントのパラメーター (デスクトップ データベース参照のアクセス)
TOCTitle: Event parameters
ms:assetid: 626de9b1-4d45-d77e-ccf2-23f2ea31c043
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249371(v=office.15)
ms:contentKeyID: 48545239
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dd4a99ec24a05084a2ae137ded3219c2997f8cf3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720493"
---
# <a name="event-parameters"></a>イベント パラメーター

**適用されます**Access 2013、Office 2013。

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

いくつかのイベント ハンドラーでは、イベントが発生した原因に関する追加情報を提供する*ため*のパラメーターがあります。 (**MoveNext**、 **MovePrevious**というように) は、ナビゲーション メソッドのいずれかが発生したため、 **WillMove**イベントと**MoveComplete**イベントを発生することがなどが呼び出された、または、再クエリの結果として。

## <a name="status-parameter"></a>ステータス パラメーター

イベント ハンドラー ルーチンが呼び出されると、*状態*のパラメーターは次の値のいずれかに設定されています。

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
<td><p>Will イベントと Complete イベントの両方に渡されます。イベントを発生させた操作が正常に完了したことを示します。</p></td>
</tr>
<tr class="even">
<td><p><strong>adStatusErrorsOccurred</strong></p></td>
<td><p>完全なイベントのみに渡されます。 この場合、イベントを発生させた操作が成功すると、できなかったこと、または Will イベントで操作がキャンセルされました。 詳細については、「<em>エラー</em>パラメーターを確認していますください。</p></td>
</tr>
<tr class="odd">
<td><p><strong>adStatusCantDeny</strong></p></td>
<td><p>Will イベントにのみ渡されます。Will イベントで操作をキャンセルできないことを示します。この操作は実行する必要があります。</p></td>
</tr>
</tbody>
</table>


判断した場合、操作を続行する必要がありますがイベントで、変更されていない*状態*のパラメーターのままにします。 受信状態のパラメーターが**adStatusCantDeny**に設定されていない限り、ただし、*ステータス*を**adStatusCancel**に変更することで、保留中の操作をキャンセルできます。 これを行うには、操作に関連付けられている完全なイベントは**adStatusErrorsOccurred**に設定されて、*ステータス*パラメーターを持ちます。 Complete イベントに渡される**Error**オブジェクトには、 **adErrOperationCancelled**の値が含まれています。

イベントを処理しない場合は、*状態*を**adStatusUnwantedEvent**に設定して、アプリケーションでは、そのイベントの通知は送信されなくなります。 ただし、理由の 1 つ以上のいくつかのイベントが発生することに注意してください。 その場合は、可能な各理由に対して**adStatusUnwantedEvent**を指定してください。 たとえば、保留中の**RecordChange**イベントの通知の受信を停止するために必要がありますパラメーターを設定する、*状態* **adRsnAddNew**、 **adRsnDelete**、 **adRsnUpdate****を**adStatusUnwantedEvent**にadRsnUndoUpdate**、 **adRsnUndoAddNew**、 **adRsnUndoDelete**、および発生するときに、その**adRsnFirstChange**です。

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

*エラー*のパラメーターは、[エラー](error-object-ado.md)の ADO オブジェクトへの参照です。 *状態*パラメーターは、 **adStatusErrorsOccurred**に設定されている場合、 **Error**オブジェクトには、操作が失敗した理由に関する詳細情報が含まれています。 Complete イベントに関連付けられた Will イベントは、*状態*のパラメーターを**adStatusCancel**に設定することにより操作がキャンセルされましたが場合、エラー オブジェクトは常に**adErrOperationCancelled**に設定します。

## <a name="object-parameter"></a>オブジェクト パラメーター

各イベントでは、操作に関係するオブジェクトを表す 1 つまたは複数のオブジェクトを受け取ります。たとえば、 **ExecuteComplete** イベントでは、 **Command** オブジェクト、 **Recordset** オブジェクト、および **Connection** オブジェクトを受け取ります。

## <a name="reason-parameter"></a>理由パラメーター

*"理由*"パラメーター *adReason*は、イベントが発生した原因に関する追加情報を提供します。 *AdReason*パラメーターを持つイベントは、別の理由で毎回、同じ操作の場合でも何回か呼び出すことができます。 たとえば、 **WillChangeRecord**イベントのハンドラーは、しようとしたりしないで、挿入、削除、またはレコードの変更を元に戻す操作に対して呼び出されます。 何らかの理由で発生したときにのみイベントを処理する場合に興味はないフィルターをかけて、 *adReason*パラメーターを使用することができます。 たとえば、レコードが追加されたために発生したときにのみ、レコードの変更イベントを処理する場合は、行うことができます次のような何か。

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

一方、 *adStatus* **adStatusUnwantedEvent**を 1 回だけを要求するイベント ハンドラーを設定せず、 **adReason**パラメーター停止イベントの通知を受信する必要があります。

