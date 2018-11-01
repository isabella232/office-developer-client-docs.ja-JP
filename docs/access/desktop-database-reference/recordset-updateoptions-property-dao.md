---
title: Recordset.UpdateOptions プロパティ (DAO)
TOCTitle: UpdateOptions Property
ms:assetid: 14ab955d-1c5a-dc76-8dbf-dbca49816bc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845468(v=office.15)
ms:contentKeyID: 48543391
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101185
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b39b9920625d970a51feadc706a3c5ff62359e53
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884353"
---
# <a name="recordsetupdateoptions-property-dao"></a><span data-ttu-id="4d3fb-102">Recordset.UpdateOptions プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d3fb-102">Recordset.UpdateOptions Property (DAO)</span></span>


<span data-ttu-id="4d3fb-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3fb-104">構文</span><span class="sxs-lookup"><span data-stu-id="4d3fb-104">Syntax</span></span>

<span data-ttu-id="4d3fb-105">*式*です。UpdateOptions</span><span class="sxs-lookup"><span data-stu-id="4d3fb-105">*expression* .UpdateOptions</span></span>

<span data-ttu-id="4d3fb-106">\*式\***レコード セット**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-106">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d3fb-107">注釈</span><span class="sxs-lookup"><span data-stu-id="4d3fb-107">Remarks</span></span>

<span data-ttu-id="4d3fb-108">バッチモードの **[Update](recordset-update-method-dao.md)** を実行すると、DAO とクライアント バッチ カーソル ライブラリによって必要な変更を行う一連の SQL UPDATE ステートメントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-108">When a batch-mode **[Update](recordset-update-method-dao.md)** is executed, DAO and the client batch cursor library create a series of SQL UPDATE statements to make the needed changes.</span></span> <span data-ttu-id="4d3fb-109">更新ごとに、 **[RecordStatus](recordset-recordstatus-property-dao.md)** プロパティによって変更済みのマークが付けられたレコードを分離する SQL WHERE 句が作成されます。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-109">An SQL WHERE clause is created for each update to isolate the records that are marked as changed by the **[RecordStatus](recordset-recordstatus-property-dao.md)** property.</span></span> <span data-ttu-id="4d3fb-110">一部のリモート サーバーではトリガーやその他の方法を使用して参照整合性を強制しているため、多くの場合、更新対象のフィールドを変更の影響を受けるフィールドのみに制限することが重要です。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-110">Because some remote servers use triggers or other ways to enforce referential integrity, is it often important to limit the fields being updated to just those affected by the change.</span></span> 

<span data-ttu-id="4d3fb-111">そのためには、 **UpdateOptions** プロパティを **dbCriteriaKey**、 **dbCriteriaModValues**、 **dbCriteriaAllCols**、 **dbCriteriaTimeStamp** のいずれかの定数に設定します。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-111">To do this, set the **UpdateOptions** property to one of the constants **dbCriteriaKey**, **dbCriteriaModValues**, **dbCriteriaAllCols**, or **dbCriteriaTimeStamp**.</span></span> <span data-ttu-id="4d3fb-112">こうすると、必要最低限のトリガー コードが実行されます。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-112">This way, only the absolute minimum amount of trigger code is executed.</span></span> <span data-ttu-id="4d3fb-113">結果として、更新操作が速くなり、エラーの可能性も少なくなります。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-113">As a result, the update operation is executed more quickly, and with fewer potential errors.</span></span>

<span data-ttu-id="4d3fb-p103">また、 **dbCriteriaDeleteInsert** 定数または **dbCriteriaUpdate** 定数を連結すると、バッチ変更をサーバーに返信する際に、各更新に対して SQL DELETE ステートメントと INSERT ステートメントのセット、または SQL UPDATE ステートメントを使用するかどうかを指定できます。前者の場合、レコードの更新には、2 つの異なる操作が必要となります。正しい **UpdateOptions** プロパティの設定を選択すると、パフォーマンスを大幅に向上させることができる場合があります (特にリモート システムに DELETE、INSERT、および UPDATE の各トリガーが実装されている場合)。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-p103">You can also concatenate either of the constants **dbCriteriaDeleteInsert** or **dbCriteriaUpdate** to determine whether to use a set of SQL DELETE and INSERT statements or an SQL UPDATE statement for each update when sending batched modifications back to the server. In the former case, two separate operations are required to update the record. In some cases, especially where the remote system implements DELETE, INSERT, and UPDATE triggers, choosing the correct **UpdateOptions** property setting can significantly impact performance.</span></span>

<span data-ttu-id="4d3fb-117">定数を指定しない場合、 **dbCriteriaUpdate** および **dbCriteriaKey** が使用されます。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-117">If you don't specify any constants, **dbCriteriaUpdate** and **dbCriteriaKey** will be used.</span></span>

<span data-ttu-id="4d3fb-118">新規レコードの追加では、常に INSERT ステートメントが生成され、レコードの削除では、常に DELETE ステートメントが生成されるため、このプロパティは、カーソル ライブラリによる変更レコードの更新の方法にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-118">Newly added records will always generate INSERT statements and deleted records will always generate DELETE statements, so this property only applies to how the cursor library updates modified records.</span></span>

## <a name="example"></a><span data-ttu-id="4d3fb-119">例</span><span class="sxs-lookup"><span data-stu-id="4d3fb-119">Example</span></span>

<span data-ttu-id="4d3fb-120">次の例では、 **BatchSize** プロパティおよび **UpdateOptions** プロパティを使用して、指定された **Recordset** オブジェクトに対するバッチ更新の諸条件を制御します。</span><span class="sxs-lookup"><span data-stu-id="4d3fb-120">This example uses the **BatchSize** and **UpdateOptions** properties to control aspects of any batch updating for the specified **Recordset** object.</span></span>

```vb 
Sub BatchSizeX() 
 
 Dim wrkMain As Workspace 
 Dim conMain As Connection 
 Dim rstTemp As Recordset 
 
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

