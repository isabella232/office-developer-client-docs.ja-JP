---
title: Visual Basic (デスクトップ データベース参照のアクセス)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3045cf3861409d2909f31536670a27c282eb2cdc
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709804"
---
# <a name="visual-basic"></a>Visual Basic


**適用されます**Access 2013、Office 2013。

Microsoft Visual Basic で ADO イベントを処理するには、 **WithEvents** キーワードを使用してモジュール レベルの変数を宣言する必要があります。この変数は、クラス モジュールの一部としてのみ宣言可能で、モジュール レベルで宣言する必要があります。しかし、Visual Basic の **Form** オブジェクトもクラスであるため、この操作は見かけほど制約的ではありません。ADO イベントを処理するための最も簡単な方法は、 **WithEvents** を使用して変数を宣言することです。 **Connection** オブジェクトの **ConnectComplete** イベントを処理する例を次に示します。

```vb 
 
' BeginEventExampleVB02 
Dim WithEvents connEvent As Connection 
Attribute connEvent.VB_VarHelpID = -1 
Dim strMsg As String 
 
Private Sub Form_Load() 
 On Error GoTo ErrHandler: 
 
 Dim strConn As String 
 
 ' Create a new object with event 
 ' handling enabled. 
 strConn = "Provider='sqloledb';" & _ 
 "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';" & _ 
 "Integrated Security='SSPI';" 
 Set connEvent = New ADODB.Connection 
 connEvent.Open strConn 
 
 Exit Sub 
 
ErrHandler: 
 MsgBox strMsg 
End Sub 
 
Private Sub connEvent_ConnectComplete(ByVal pError As ADODB.Error, _ 
 adStatus As ADODB.EventStatusEnum, _ 
 ByVal pConnection As ADODB.Connection) 
 
 If adStatus = adStatusErrorsOccurred Then 
 If Not pError Is Nothing Then 
 Select Case pError.Number 
 Case adErrOperationCancelled 
 ' The operation was cancelled in the 
 ' Will event. Notify the user and exit. 
 strMsg = "I'm sorry you can't connect right now." & vbCrLf 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 Case Else 
 strMsg = "Error " & Format(pError.Number) & vbCrLf 
 strMsg = strMsg & pError.Description 
 strMsg = strMsg & " Click OK to exit." 
 Unload Me 
 End Select 
 Else 
 strMsg = "Error occured. Click OK to exit." 
 Unload Me 
 End If 
 End If 
 'frmWait.btnOK.Enabled = True 
End Sub 
' EndEventExampleVB02 
```

イベント処理を有効にするため、 **Connection** オブジェクトが **WithEvents** キーワードを使用して **Form** レベルで宣言されています。 フォーム\_Load イベント ハンドラーは、実際に新しい**接続**オブジェクトを*connEvent*に割り当てることによってオブジェクトが作成され、接続を開きます。 実際のアプリケーションでは、もちろんは、フォーム内のより多くの処理の操作を行います\_よりも、次のように、Load イベント ハンドラーです。

