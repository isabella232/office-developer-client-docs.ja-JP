---
title: Connection.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 565dff4e1592ef431aad0c7cb1daa581520f73ec
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479526"
---
# <a name="connectioncancel-method-dao"></a>Connection.Cancel メソッド (DAO)

**適用されます**Access 2013 |。Office 2013

## <a name="syntax"></a>構文

*式*です。キャンセル

*式***接続**オブジェクトを表す変数です。

## <a name="remarks"></a>備考

**Cancel**メソッドを使用して、**実行**または**されます**メソッドの非同期呼び出しの実行を中止する (つまり、メソッドが dbRunAsync オプションを指定して呼び出されました)。 終了するメソッドで dbRunAsync が使用できない場合、**キャンセル**実行時エラー戻ります。

**Cancel** メソッドを呼び出した後に、非同期の **OpenConnection** の呼び出しによって作成されたオブジェクト ( **Cancel** メソッドを呼び出した **Connection** オブジェクト) を参照しようとすると、エラーが発生します。

## <a name="example"></a>例

次の例では、 **StillExecuting** プロパティと **Cancel** メソッドを使用して、 **Connection** オブジェクトを非同期で開きます。

```vb
    Sub CancelConnectionX() 
     
     Dim wrkMain As Workspace 
     Dim conMain As Connection 
     Dim sngTime As Single 
     
     Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
     "admin", "", dbUseODBC) 
     ' Open the connection asynchronously. 
     
     ' Note: The DSN referenced below must be configured to 
     ' use Microsoft Windows NT Authentication Mode to 
     ' authorize user access to the Microsoft SQL Server. 
     Set conMain = wrkMain.OpenConnection("Publishers", _ 
     dbDriverNoPrompt + dbRunAsync, False, _ 
     "ODBC;DATABASE=pubs;DSN=Publishers") 
     
     sngTime = Timer 
     
     ' Wait five seconds. 
     Do While Timer - sngTime < 5 
     Loop 
     
     ' If the connection has not been made, ask the user 
     ' if she wants to keep waiting. If she does not, cancel 
     ' the connection and exit the procedure. 
     Do While conMain.StillExecuting 
     
     If MsgBox("No connection yet--keep waiting?", _ 
     vbYesNo) = vbNo Then 
     conMain.Cancel 
     MsgBox "Connection cancelled!" 
     wrkMain.Close 
     Exit Sub 
     End If 
     
     Loop 
     
     With conMain 
     ' Use the Connection object conMain. 
     .Close 
     End With 
     
     wrkMain.Close 
     
    End Sub
```
