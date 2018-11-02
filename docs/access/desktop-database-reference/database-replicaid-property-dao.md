---
title: Database.ReplicaID プロパティ (DAO)
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
ms.openlocfilehash: 3214f093b90576483df4d6f63cf1ad62b3530931
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25918766"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="560ea-102">Database.ReplicaID プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="560ea-102">Database.ReplicaID property (DAO)</span></span>


<span data-ttu-id="560ea-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="560ea-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="560ea-104">データベース レプリカを一意に識別する 16 バイトの値を取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="560ea-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="560ea-105">構文</span><span class="sxs-lookup"><span data-stu-id="560ea-105">Syntax</span></span>

<span data-ttu-id="560ea-106">*式*です。ReplicaID</span><span class="sxs-lookup"><span data-stu-id="560ea-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="560ea-107">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="560ea-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="560ea-108">注釈</span><span class="sxs-lookup"><span data-stu-id="560ea-108">Remarks</span></span>

<span data-ttu-id="560ea-109">戻り値は、レプリカまたはデザイン マスターを一意に識別する GUID 型 ( **GUID**) の値です。</span><span class="sxs-lookup"><span data-stu-id="560ea-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="560ea-110">Microsoft Access データベース エンジンは、新規レプリカの作成時にこの値を自動的に生成します。</span><span class="sxs-lookup"><span data-stu-id="560ea-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="560ea-111">各レプリカ (およびデザイン マスター) の **ReplicaID** プロパティは、MSysReplicas システム テーブルに保存されます。</span><span class="sxs-lookup"><span data-stu-id="560ea-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="560ea-112">例</span><span class="sxs-lookup"><span data-stu-id="560ea-112">Example</span></span>

<span data-ttu-id="560ea-p101">この例では、Northwind.mdb のデザイン マスターからレプリカを作成し、Microsoft Access データベース エンジンによって自動的に作成されるレプリカの **ReplicaID** を返します (Northwind のデザイン マスターをまだ作成していない場合は、 **Replicable** プロパティを参照するか、コード内のデータベース名を既存のデザイン マスターに変更します)。</span><span class="sxs-lookup"><span data-stu-id="560ea-p101">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

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

