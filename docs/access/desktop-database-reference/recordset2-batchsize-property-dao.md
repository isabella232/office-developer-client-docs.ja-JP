---
title: Recordset2.BatchSize プロパティ (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3ab4a22bc3c86e89addd07d3fabe7d5ce0e8bc3
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921279"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="a5f83-102">Recordset2.BatchSize プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="a5f83-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="a5f83-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a5f83-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f83-104">構文</span><span class="sxs-lookup"><span data-stu-id="a5f83-104">Syntax</span></span>

<span data-ttu-id="a5f83-105">*式*です。BatchSize</span><span class="sxs-lookup"><span data-stu-id="a5f83-105">*expression* .BatchSize</span></span>

<span data-ttu-id="a5f83-106">\*式\***Recordset2**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="a5f83-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5f83-107">注釈</span><span class="sxs-lookup"><span data-stu-id="a5f83-107">Remarks</span></span>

<span data-ttu-id="a5f83-p101">**BatchSize** プロパティは、バッチ更新でステートメントをサーバーに送信するときに使用されるバッチ サイズを決定します。このプロパティの値は、1 つのコマンド バッファーでサーバーに送信されるステートメントの数を決定します。既定では、各バッチで 15 個のステートメントがサーバーに送信されます。このプロパティはいつでも変更できます。データベース サーバーがステートメントのバッチ処理をサポートしていない場合、このプロパティを 1 に設定すると、各ステートメントが個別に送信されます。</span><span class="sxs-lookup"><span data-stu-id="a5f83-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="a5f83-113">例</span><span class="sxs-lookup"><span data-stu-id="a5f83-113">Example</span></span>

<span data-ttu-id="a5f83-114">次の使用例は、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定した Recordset オブジェクトの任意のバッチ更新の環境を制御します。</span><span class="sxs-lookup"><span data-stu-id="a5f83-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

```vb
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 
 Set wrkMain = CreateWorkspace("ODBCWorkspace", _ 
 "admin", "", dbUseODBC) 
 ' This DefaultCursorDriver setting is required for 
 ' batch updating. 
 wrkMain.DefaultCursorDriver = dbUseClientBatchCursor 
 
 ' Note: The DSN referenced below must be configured to 
 ' use Microsoft Windows NT Authentication Mode to 
 ' authorize user access to the Microsoft SQL Server. 
 Set conMain = wrkMain.OpenConnection("Publishers", _ 
 dbDriverNoPrompt, False, _ 
 "ODBC;DATABASE=pubs;DSN=Publishers") 
 
 ' The following locking argument is required for 
 ' batch updating. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Increase the number of statements sent to the server 
 ' during a single batch update, thereby reducing the 
 ' number of times an update would have to access the 
 ' server. 
 .BatchSize = 25 
 
 ' Change the UpdateOptions property so that the WHERE 
 ' clause of any batched statements going to the server 
 ' will include any updated columns in addition to the 
 ' key column(s). Also, any modifications to records 
 ' will be made by deleting the original record 
 ' and adding a modified version rather than just 
 ' modifying the original record. 
 .UpdateOptions = dbCriteriaModValues + _ 
 dbCriteriaDeleteInsert 
 
 ' Engage in batch updating using the new settings 
 ' above. 
 ' ... 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

