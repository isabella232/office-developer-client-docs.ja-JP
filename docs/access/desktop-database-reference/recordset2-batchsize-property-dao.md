---
title: Recordset2 プロパティ (DAO)
TOCTitle: BatchSize Property
ms:assetid: fa7f12f6-36c8-5aad-31d2-668cfe46f9f7
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837054(v=office.15)
ms:contentKeyID: 48548846
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f615823f99e2fdaa50a051d89a90c8f85a6ec841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307470"
---
# <a name="recordset2batchsize-property-dao"></a><span data-ttu-id="98948-102">Recordset2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="98948-102">Recordset2.BatchSize property (DAO)</span></span>


<span data-ttu-id="98948-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="98948-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="98948-104">構文</span><span class="sxs-lookup"><span data-stu-id="98948-104">Syntax</span></span>

<span data-ttu-id="98948-105">*式*。BatchSize</span><span class="sxs-lookup"><span data-stu-id="98948-105">*expression* .BatchSize</span></span>

<span data-ttu-id="98948-106">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="98948-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="98948-107">注釈</span><span class="sxs-lookup"><span data-stu-id="98948-107">Remarks</span></span>

<span data-ttu-id="98948-p101">**BatchSize** プロパティを使用すると、一括更新でサーバーにステートメントを送信するときに使用するバッチ サイズを指定できます。このプロパティの値によって、1 つのコマンド バッファーでサーバーに送信されるステートメントの数が決まります。既定では、それぞれのバッチで 15 ステートメントがサーバーに送信されます。このプロパティはいつでも変更できます。データベース サーバーがステートメントのバッチ処理をサポートしていない場合、このプロパティを 1 に設定すると、それぞれのステートメントを個別に送信できます。</span><span class="sxs-lookup"><span data-stu-id="98948-p101">The **BatchSize** property determines the batch size used when sending statements to the server in a batch update. The value of the property determines the number of statements sent to the server in one command buffer. By default, 15 statements are sent to the server in each batch. This property can be changed at any time. If a database server doesn't support statement batching, you can set this property to 1, causing each statement to be sent separately.</span></span>

## <a name="example"></a><span data-ttu-id="98948-113">例</span><span class="sxs-lookup"><span data-stu-id="98948-113">Example</span></span>

<span data-ttu-id="98948-114">この例では、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定した Recordset オブジェクトに対する一括更新の要素を制御します。</span><span class="sxs-lookup"><span data-stu-id="98948-114">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified Recordset object.</span></span>

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

