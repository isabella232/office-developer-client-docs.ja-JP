---
title: BatchCollisionCount プロパティ (DAO)
TOCTitle: BatchCollisionCount Property
ms:assetid: 997dfbb3-673c-8813-f51b-ab8d95093c4f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197961(v=office.15)
ms:contentKeyID: 48546514
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 33650b9fdbaf7fbc9266c8c778199e1138cd5b21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307484"
---
# <a name="recordset2batchcollisioncount-property-dao"></a><span data-ttu-id="819a3-102">BatchCollisionCount プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="819a3-102">Recordset2.BatchCollisionCount property (DAO)</span></span>


<span data-ttu-id="819a3-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="819a3-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="819a3-104">構文</span><span class="sxs-lookup"><span data-stu-id="819a3-104">Syntax</span></span>

<span data-ttu-id="819a3-105">*式*。BatchCollisionCount</span><span class="sxs-lookup"><span data-stu-id="819a3-105">*expression* .BatchCollisionCount</span></span>

<span data-ttu-id="819a3-106">\*式\***Recordset2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="819a3-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="819a3-107">注釈</span><span class="sxs-lookup"><span data-stu-id="819a3-107">Remarks</span></span>

<span data-ttu-id="819a3-p101">このプロパティは、最後の一括更新を実行しているときに競合が発生したかまたは更新に失敗したレコードの数を示します。このプロパティの値は、 **[BatchCollisions](recordset2-batchcollisions-property-dao.md)** プロパティ内のブックマークの数と一致します。</span><span class="sxs-lookup"><span data-stu-id="819a3-p101">This property indicates how many records encountered collisions or otherwise failed to update during the last batch update attempt. The value of this property corresponds to the number of bookmarks in the **[BatchCollisions](recordset2-batchcollisions-property-dao.md)** property.</span></span>

<span data-ttu-id="819a3-110">作業中の **Recordset** オブジェクトの **[Bookmark](recordset2-bookmark-property-dao.md)** プロパティを **BatchCollisions** 配列のブックマーク値に設定すると、最後のバッチ **[Update](recordset2-update-method-dao.md)** 操作で更新を完了できなかった各レコードに移動できます。</span><span class="sxs-lookup"><span data-stu-id="819a3-110">If you set the working **Recordset** object's **[Bookmark](recordset2-bookmark-property-dao.md)** property to bookmark values in the **BatchCollisions** array, you can move to each record that failed to complete the most recent batch **[Update](recordset2-update-method-dao.md)** operation.</span></span>

<span data-ttu-id="819a3-p102">競合が発生したレコードを修正した後、もう一度バッチ モードの **Update** メソッドを呼び出すことができます。この時点で DAO は再度一括更新を試み、この 2 回目の更新に失敗したレコードのセットが、もう一度 **BatchCollisions** プロパティに反映されます。前回の処理で更新に成功したレコードは、 **[RecordStatus](recordset2-recordstatus-property-dao.md)** プロパティが **dbRecordUnmodified** に設定されているため、2 回目の更新の対象から除外されます。この処理は、競合が発生している限り続行するか、または更新を中止して結果セットを閉じるまで続行できます。</span><span class="sxs-lookup"><span data-stu-id="819a3-p102">After the collision records are corrected, a batch-mode **Update** method can be called again. At this point DAO attempts another batch update, and the **BatchCollisions** property again reflects the set of records that failed the second attempt. Any records that succeeded in the previous attempt are not sent in the current attempt, because they now have a **[RecordStatus](recordset2-recordstatus-property-dao.md)** property of **dbRecordUnmodified**. This process can continue as long as collisions occur, or until you abandon the updates and close the result set.</span></span>

## <a name="example"></a><span data-ttu-id="819a3-115">例</span><span class="sxs-lookup"><span data-stu-id="819a3-115">Example</span></span>

<span data-ttu-id="819a3-116">この例では、 **BatchCollisionCount** プロパティおよび **Update** メソッドを使用して一括更新を実行し、その一括更新ですべての競合を解決する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="819a3-116">This example uses the **BatchCollisionCount** property and the **Update** method to demonstrate batch updating where any collisions are resolved by forcing the batch update.</span></span>

```vb 
Sub BatchX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset2 
 Dim intLoop As Integer 
 Dim strPrompt As String 
 
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
 ' batch updating. It is also required that a table 
 ' with a primary key is used. 
 Set rstTemp = conMain.OpenRecordset( _ 
 "SELECT * FROM roysched", dbOpenDynaset, 0, _ 
 dbOptimisticBatch) 
 
 With rstTemp 
 ' Modify data in local recordset. 
 Do While Not .EOF 
 .Edit 
 If !royalty <= 20 Then 
 !royalty = !royalty - 4 
 Else 
 !royalty = !royalty + 2 
 End If 
 .Update 
 .MoveNext 
 Loop 
 
 ' Attempt a batch update. 
 .Update dbUpdateBatch 
 
 ' If there are collisions, give the user the option 
 ' of forcing the changes or resolving them 
 ' individually. 
 If .BatchCollisionCount > 0 Then 
 strPrompt = "There are collisions. " & vbCr & _ 
 "Do you want the program to force " & _ 
 vbCr & "an update using the local data?" 
 If MsgBox(strPrompt, vbYesNo) = vbYes Then _ 
 .Update dbUpdateBatch, True 
 End If 
 
 .Close 
 End With 
 
 conMain.Close 
 wrkMain.Close 
 
End Sub 
 
```

