---
title: Visual Basic (Access デスクトップデータベースリファレンス)
TOCTitle: Visual Basic
ms:assetid: 9d153b6c-c860-7350-cb3c-b9bd08f75ba8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249714(v=office.15)
ms:contentKeyID: 48546616
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3045cf3861409d2909f31536670a27c282eb2cdc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312139"
---
# <a name="visual-basic"></a><span data-ttu-id="2d5f9-102">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="2d5f9-102">Visual Basic</span></span>


<span data-ttu-id="2d5f9-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d5f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d5f9-p101">Microsoft Visual Basic で ADO イベントを処理するには、 **WithEvents** キーワードを使用してモジュール レベルの変数を宣言する必要があります。この変数は、クラス モジュールの一部としてのみ宣言可能で、モジュール レベルで宣言する必要があります。しかし、Visual Basic の **Form** オブジェクトもクラスであるため、この操作は見かけほど制約的ではありません。ADO イベントを処理するための最も簡単な方法は、 **WithEvents** を使用して変数を宣言することです。 **Connection** オブジェクトの **ConnectComplete** イベントを処理する例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="2d5f9-p101">In order to handle ADO events in Microsoft Visual Basic, you must declare a module-level variable using the **WithEvents** keyword. The variable can be declared only as part of a class module and must be declared at the module level. This is not as restrictive as it seems, however, because Visual Basic **Form** objects are also classes. The simplest way to handle ADO events is to declare a variable using **WithEvents**. The following example handles the **ConnectComplete** event for a **Connection** object:</span></span>

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

<span data-ttu-id="2d5f9-109">イベント処理を有効にするため、 **Connection** オブジェクトが **WithEvents** キーワードを使用して **Form** レベルで宣言されています。</span><span class="sxs-lookup"><span data-stu-id="2d5f9-109">The **Connection** object is declared at the **Form** level using the **WithEvents** keyword to enable event handling.</span></span> <span data-ttu-id="2d5f9-110">Form\_Load イベントハンドラーは、 *connEvent*に新しい**connection**オブジェクトを割り当て、その接続を開くことにより、実際にオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2d5f9-110">The Form\_Load event handler actually creates the object by assigning a new **Connection** object to *connEvent* and then opens the connection.</span></span> <span data-ttu-id="2d5f9-111">当然のことですが、実際のアプリケーションでは、次\_に示すより多くの処理が Form Load イベントハンドラーで行われます。</span><span class="sxs-lookup"><span data-stu-id="2d5f9-111">Of course, a real application would do more processing in the Form\_Load event handler than is shown here.</span></span>

