---
title: Relation レプリカプロパティ (DAO)
TOCTitle: PartialReplica Property
ms:assetid: 3cb15639-371e-06e3-e2ba-30466ce09a72
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192692(v=office.15)
ms:contentKeyID: 48544324
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053557
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: fef48902b806f13947ae4b81728af4c5704c2b8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307015"
---
# <a name="relationpartialreplica-property-dao"></a><span data-ttu-id="c4edb-102">Relation レプリカプロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="c4edb-102">Relation.PartialReplica property (DAO)</span></span>

<span data-ttu-id="c4edb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="c4edb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c4edb-p101">フル レプリカから部分レプリカに値を設定するときに、 **Relation** オブジェクトのリレーションシップを考慮する必要があるかどうかを示す値を設定または取得します (Microsoft Access データベース エンジンのデータベースのみ)。値の取得および設定が可能です。ブール型 ( **Boolean**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c4edb-p101">Sets or returns a value on a **Relation** object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write **Boolean**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4edb-107">構文</span><span class="sxs-lookup"><span data-stu-id="c4edb-107">Syntax</span></span>

<span data-ttu-id="c4edb-108">*式*。PartialReplica</span><span class="sxs-lookup"><span data-stu-id="c4edb-108">*expression* .PartialReplica</span></span>

<span data-ttu-id="c4edb-109">\*式\***Relation**オブジェクトを返す式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c4edb-109">*expression* An expression that returns a **Relation** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4edb-110">注釈</span><span class="sxs-lookup"><span data-stu-id="c4edb-110">Remarks</span></span>

<span data-ttu-id="c4edb-111">設定値または戻り値はブール型 (Boolean) の値で、同期時にこのリレーションシップを適用する必要がある場合は **True** です。</span><span class="sxs-lookup"><span data-stu-id="c4edb-111">The setting or return value is a Boolean data type that is **True** when the relation should be enforced during synchronization.</span></span>

<span data-ttu-id="c4edb-112">このプロパティを使用すると、テーブル間のリレーションシップに基づいて、フル レプリカのデータを部分レプリカにレプリケートできます。</span><span class="sxs-lookup"><span data-stu-id="c4edb-112">This property enables you to replicate data from the full replica to the partial replica based on relationships between tables.</span></span> <span data-ttu-id="c4edb-113">**ReplicaFilter** プロパティの設定のみでは部分レプリカにレプリケートする必要のあるデータを適切に指定できない場合に、 **PartialReplica** プロパティを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4edb-113">You can use the **PartialReplica** property when setting the **ReplicaFilter** property alone can't adequately specify what data should be replicated to the partial.</span></span> <span data-ttu-id="c4edb-114">たとえば、顧客テーブルが注文テーブルと一対多のリレーションシップを持つデータベースがあり、すべての注文ではなくカリフォルニア地域の顧客からの注文のみをレプリケートする部分レプリカを構成するとします。</span><span class="sxs-lookup"><span data-stu-id="c4edb-114">For example, suppose you have a database in which the Customers table has a one-to-many relationship with the Orders table, and you want to configure a partial replica that only replicates orders from customers in the California region (instead of all orders).</span></span> <span data-ttu-id="c4edb-115">Region フィールドは注文テーブルではなく顧客テーブルにあるため、注文テーブルの **ReplicaFilter** プロパティを Region = 'CA' に設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="c4edb-115">It is not possible to set the **ReplicaFilter** property on the Orders table to Region = 'CA' because the Region field is in the Customers table, not the Orders table.</span></span>

<span data-ttu-id="c4edb-p103">カリフォルニア地域からのすべての注文をレプリケートするには、レプリケーション時に注文テーブルと顧客テーブル間のリレーションシップがアクティブになるように指定する必要があります。部分レプリカを作成した後、以下の手順を実行すると、カリフォルニア地域からのすべての注文が部分レプリカに設定されます。</span><span class="sxs-lookup"><span data-stu-id="c4edb-p103">To replicate all orders from the California region, you must indicate that the relation between the Orders and Customers tables will be active during replication. Once you've created a partial replica, the following steps will populate it with all orders from the California region:</span></span>

1.  <span data-ttu-id="c4edb-118">Customers **TableDef**オブジェクトの**ReplicaFilter**プロパティを "Region = ' CA '" に設定します。</span><span class="sxs-lookup"><span data-stu-id="c4edb-118">Set the **ReplicaFilter** property on the Customers **TableDef** object to "Region = 'CA'".</span></span>

2.  <span data-ttu-id="c4edb-119">注文テーブルと顧客テーブル間のリレーションシップに対応する **Relation** オブジェクトの **PartialReplica** プロパティの値を **True** に設定します。</span><span class="sxs-lookup"><span data-stu-id="c4edb-119">Set the value of the **PartialReplica** property to **True** on the **Relation** object corresponding to the relationship between Orders and Customers.</span></span>

3.  <span data-ttu-id="c4edb-120">**PopulatePartial** メソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="c4edb-120">Invoke the **PopulatePartial** method.</span></span>
    

> [!NOTE]
> <span data-ttu-id="c4edb-121">[!メモ] レプリカ フィルターまたはレプリカ リレーションシップを設定した場合、部分レプリカ内の制限条件を満たさないレコードは部分レプリカから削除されますが、フル レプリカからは削除されません。</span><span class="sxs-lookup"><span data-stu-id="c4edb-121">When you set a replica filter or replica relation, be aware that records in the partial replica that don't satisfy the restriction criteria will be removed from the partial replica, but not from the full replica.</span></span> <span data-ttu-id="c4edb-122">たとえば、部分レプリカの顧客 **TableDef** オブジェクトの **ReplicaFilter** プロパティを "Region = 'CA'" に設定し、データベースにもう一度値を設定するとします。</span><span class="sxs-lookup"><span data-stu-id="c4edb-122">For example, suppose you set the **ReplicaFilter** property on the Customers **TableDef** in the partial replica to "Region = 'CA'" and you then repopulate the database.</span></span> <span data-ttu-id="c4edb-123">これにより、カリフォルニア地域の顧客のすべてのレコードが挿入または更新されます。</span><span class="sxs-lookup"><span data-stu-id="c4edb-123">This will insert or update all records for California-based customers.</span></span> 
> 
> <span data-ttu-id="c4edb-124">次に、**ReplicaFilter** プロパティを "Region = 'FL'" に再設定し、データベースにもう一度値を設定すると、部分レプリカ内にあるカリフォルニア地域のすべてのレコードが削除され、フル レプリカからフロリダ地域の顧客のすべてのレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="c4edb-124">If you then reset the **ReplicaFilter** property to "Region = 'FL'" and repopulate the database, all California region records in the partial replica will be removed, and all records from Florida-based customers will be inserted from the full replica.</span></span> <span data-ttu-id="c4edb-125">フル レプリカ内のレコードは削除されません。</span><span class="sxs-lookup"><span data-stu-id="c4edb-125">No records in the full replica will be deleted.</span></span> 
>
> <span data-ttu-id="c4edb-126">**ReplicaFilter** プロパティまたは **PartialReplica** プロパティを設定する前に、これらのプロパティを設定する部分レプリカをフル レプリカと同期させることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c4edb-126">Before setting either the **ReplicaFilter** or **PartialReplica** property, it's a good idea to synchronize the partial replica in which you are setting these properties with the full replica.</span></span> <span data-ttu-id="c4edb-127">これにより、部分レプリカ内のすべてのレコードが削除される前に、部分レプリカの保留中の変更がフル レプリカに反映されます。</span><span class="sxs-lookup"><span data-stu-id="c4edb-127">This will ensure that pending changes in the partial replica will be merged into the full replica before any records are removed in the partial replica.</span></span>


