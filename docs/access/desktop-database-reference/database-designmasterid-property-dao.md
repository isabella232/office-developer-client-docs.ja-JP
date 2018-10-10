---
title: Database.DesignMasterID プロパティ (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0bb2e369f886ba60fb425b9f1f2d10fdea0c1463
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477940"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="455f6-102">Database.DesignMasterID プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="455f6-102">Database.DesignMasterID Property (DAO)</span></span>

<span data-ttu-id="455f6-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="455f6-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="455f6-104">レプリカ セットでデザイン マスターを一意に識別する 16 バイトの値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="455f6-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="455f6-105">構文</span><span class="sxs-lookup"><span data-stu-id="455f6-105">Syntax</span></span>

<span data-ttu-id="455f6-106">*式*です。DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="455f6-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="455f6-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="455f6-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="455f6-108">注釈</span><span class="sxs-lookup"><span data-stu-id="455f6-108">Remarks</span></span>

<span data-ttu-id="455f6-p101">**DesignMasterID** プロパティを設定するのは、現在のデザイン マスターを移動する必要がある場合のみです。このプロパティを設定すると、レプリカ セットの特定のレプリカがデザイン マスターになります。</span><span class="sxs-lookup"><span data-stu-id="455f6-p101">You should set the **DesignMasterID** property only if you need to move the current Design Master. Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="455f6-p102">[!メモ] レプリカ セットで 2 つ目のデザイン マスターを作成しないでください。2 つ目のデザイン マスターが存在すると、データが失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="455f6-p102">Never create a second Design Master in a replica set. The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="455f6-p103">デザイン マスターの削除や破損などの特殊な状況下では、現在のレプリカでこのプロパティを設定できます。ただし、レプリカ セットに既に別のデザイン マスターが存在するときに、レプリカでこのプロパティを設定すると、レプリカ セットが 2 つの調整不可能なセットに分割され、それ以降のデータの同期が行われなくなる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="455f6-p103">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica. However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="455f6-p104">レプリカをセットの新しいデザイン マスターにする場合は、レプリカ セットのすべてのレプリカと同期してから、レプリカの **DesignMasterID** プロパティを設定します。レプリカをデザイン マスターにするには、レプリカを排他モードで開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="455f6-p104">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica. The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="455f6-117">読み取り専用として指定されているレプリカをデザイン マスターにすると、対象のレプリカは読み取り/書き込みが可能になり、古いデザイン マスターも引き続き読み取り/書き込みが可能です。</span><span class="sxs-lookup"><span data-stu-id="455f6-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="455f6-118">**DesignMasterID** プロパティの設定値は、MSysRepInfo システム テーブルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="455f6-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="455f6-119">例</span><span class="sxs-lookup"><span data-stu-id="455f6-119">Example</span></span>

<span data-ttu-id="455f6-p105">次の使用例は、 **DesignMasterID** プロパティを別のデータベースの **ReplicaID** プロパティの設定値に設定し、そのデータベースをレプリカ セットのデザイン マスターにします。新旧のデザイン マスターが同期されて、デザインの変更が更新されます。このコードが機能するには、デザイン マスターとレプリカを作成し、必要に応じてその名前とパスを含め、このコードを新旧のデザイン マスター以外のデータベースから実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="455f6-p105">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set. The old and new Design Masters are synchronized to update the design change. For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```
