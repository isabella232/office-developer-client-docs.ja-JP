---
title: Connection.StillExecuting プロパティ (DAO)
TOCTitle: StillExecuting Property
ms:assetid: 0121f98a-cc23-5b5e-9a75-28307404a9a3
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844743(v=office.15)
ms:contentKeyID: 48542927
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 616e2bc6e374d7aba17c5cd07030469d8941014c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719933"
---
# <a name="connectionstillexecuting-property-dao"></a><span data-ttu-id="d8fde-102">Connection.StillExecuting プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="d8fde-102">Connection.StillExecuting property (DAO)</span></span>

<span data-ttu-id="d8fde-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d8fde-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d8fde-104">構文</span><span class="sxs-lookup"><span data-stu-id="d8fde-104">Syntax</span></span>

<span data-ttu-id="d8fde-105">*式*です。StillExecuting</span><span class="sxs-lookup"><span data-stu-id="d8fde-105">*expression* .StillExecuting</span></span>

<span data-ttu-id="d8fde-106">\*式\***接続**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="d8fde-106">*expression* A variable that represents a **Connection** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8fde-107">注釈</span><span class="sxs-lookup"><span data-stu-id="d8fde-107">Remarks</span></span>

<span data-ttu-id="d8fde-p101">**StillExecuting** プロパティを使用して、直前に呼び出した非同期の **Execute** メソッドまたは **OpenConnection** メソッド (つまり、 **dbRunAsync** オプションを指定して実行したメソッド) が完了しているかどうかを調べます。 **StillExecuting** プロパティが **True** の間は、返されたオブジェクトにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="d8fde-p101">Use the **StillExecuting** property to determine if the most recently called asynchronous **Execute** or **OpenConnection** method (that is, a method executed with the **dbRunAsync** option) is complete. While the **StillExecuting** property is **True**, any returned object cannot be accessed.</span></span>

<span data-ttu-id="d8fde-p102">**StillExecuting** プロパティで **False** が取得された後で、関連付けられた **Connection** オブジェクトを返す **OpenConnection** メソッドを呼び出すと、そのオブジェクトを参照できます。 **StillExecuting** で **True** が取得される間は、 **StillExecuting** プロパティの取得を除き、そのオブジェクトに対する参照は実行できません。</span><span class="sxs-lookup"><span data-stu-id="d8fde-p102">Once the **StillExecuting** property returns **False**, following the **OpenConnection** call that returns the associated **Connection** object, the object can be referenced. So long as **StillExecuting** remains **True**, the object may not be referenced, other than to read the **StillExecuting** property.</span></span>

<span data-ttu-id="d8fde-112">進行中のタスクの実行を中止するには、 **[Cancel](connection-cancel-method-dao.md)** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d8fde-112">Use the **[Cancel](connection-cancel-method-dao.md)** method to terminate execution of a task in progress.</span></span>

## <a name="example"></a><span data-ttu-id="d8fde-113">例</span><span class="sxs-lookup"><span data-stu-id="d8fde-113">Example</span></span>

<span data-ttu-id="d8fde-114">次の例では、 **StillExecuting** プロパティと **Cancel** メソッドを使用して、 **Connection** オブジェクトを非同期で開きます。</span><span class="sxs-lookup"><span data-stu-id="d8fde-114">This example uses the **StillExecuting** property and the **Cancel** method to asynchronously open a **Connection** object.</span></span>

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
