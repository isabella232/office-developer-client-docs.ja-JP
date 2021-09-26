---
title: Connection.Cancel メソッド (DAO)
TOCTitle: Cancel Method
ms:assetid: 43ad7b64-823d-3fac-e4d4-5e9514f60011
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192953(v=office.15)
ms:contentKeyID: 48544509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 489f1d1b85fdd9a3ba207f733123cf18af6c91d5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597612"
---
# <a name="connectioncancel-method-dao"></a>Connection.Cancel メソッド (DAO)

**適用先**: Access 2013、Office 2013

## <a name="syntax"></a>構文

*式* .キャンセル

*式***Connection** オブジェクトを表す変数です。

## <a name="remarks"></a>注釈

Cancel メソッド **を使用** して、非同期の **Execute** メソッドまたは **OpenConnection** メソッド呼び出しの実行を終了します (つまり、メソッドは dbRunAsync オプションを使用して呼び出されました)。 **Cancel** は、終了しようとしているメソッドで dbRunAsync が使用されていない場合、実行時エラーを返します。

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
