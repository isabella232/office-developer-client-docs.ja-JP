---
title: データベースの ReplicaID プロパティ (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294716"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="eb434-102">データベースの ReplicaID プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="eb434-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="eb434-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="eb434-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="eb434-104">データベース レプリカを一意に識別する 16 バイトの値を取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="eb434-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb434-105">構文</span><span class="sxs-lookup"><span data-stu-id="eb434-105">Syntax</span></span>

<span data-ttu-id="eb434-106">*式*。ReplicaID</span><span class="sxs-lookup"><span data-stu-id="eb434-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="eb434-107">\*式\***Database**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="eb434-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb434-108">注釈</span><span class="sxs-lookup"><span data-stu-id="eb434-108">Remarks</span></span>

<span data-ttu-id="eb434-109">戻り値は、レプリカまたはデザイン マスターを一意に識別する GUID 型 ( **GUID**) の値です。</span><span class="sxs-lookup"><span data-stu-id="eb434-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="eb434-110">Microsoft Access データベース エンジンは、新規レプリカの作成時にこの値を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="eb434-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="eb434-111">各レプリカ (およびデザイン マスター) の **ReplicaID** プロパティは、MSysReplicas システム テーブルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="eb434-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="eb434-112">例</span><span class="sxs-lookup"><span data-stu-id="eb434-112">Example</span></span>

<span data-ttu-id="eb434-p101">この例では、Northwind.mdb のデザイン マスターからレプリカを作成し、Microsoft Access データベース エンジンによって自動的に作成されるレプリカの **ReplicaID** を返します (Northwind のデザイン マスターをまだ作成していない場合は、 **Replicable** プロパティを参照するか、コード内のデータベース名を既存のデザイン マスターに変更します)。</span><span class="sxs-lookup"><span data-stu-id="eb434-p101">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

