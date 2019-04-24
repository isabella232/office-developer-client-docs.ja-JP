---
title: Database. Synchronize メソッド (DAO)
TOCTitle: Synchronize Method
ms:assetid: 5e716a4a-2430-8106-5c34-a02dd28bc4f6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194659(v=office.15)
ms:contentKeyID: 48545137
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053357
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 411948f3c0ac4d6c353cd2722136dffb6a25fb17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294709"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="a30cb-102">Database. Synchronize メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="a30cb-102">Database.Synchronize method (DAO)</span></span>


<span data-ttu-id="a30cb-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a30cb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a30cb-p101">2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="a30cb-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="a30cb-106">構文</span><span class="sxs-lookup"><span data-stu-id="a30cb-106">Syntax</span></span>

<span data-ttu-id="a30cb-107">*式*。Synchronize (***dbpathname***, ***ExchangeType***)</span><span class="sxs-lookup"><span data-stu-id="a30cb-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="a30cb-108">\*式\***Database**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="a30cb-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="a30cb-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a30cb-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a30cb-110">名前</span><span class="sxs-lookup"><span data-stu-id="a30cb-110">Name</span></span></p></th>
<th><p><span data-ttu-id="a30cb-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="a30cb-111">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="a30cb-112">データ型</span><span class="sxs-lookup"><span data-stu-id="a30cb-112">Data type</span></span></p></th>
<th><p><span data-ttu-id="a30cb-113">説明</span><span class="sxs-lookup"><span data-stu-id="a30cb-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a30cb-114"><em>DbPathName</em></span><span class="sxs-lookup"><span data-stu-id="a30cb-114"><em>DbPathName</em></span></span></p></td>
<td><p><span data-ttu-id="a30cb-115">必須</span><span class="sxs-lookup"><span data-stu-id="a30cb-115">Required</span></span></p></td>
<td><p><span data-ttu-id="a30cb-116"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="a30cb-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="a30cb-117">データベースを同期させる対象のレプリカへのパスです。</span><span class="sxs-lookup"><span data-stu-id="a30cb-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a30cb-118"><em>ExchangeType</em></span><span class="sxs-lookup"><span data-stu-id="a30cb-118"><em>ExchangeType</em></span></span></p></td>
<td><p><span data-ttu-id="a30cb-119">Optional</span><span class="sxs-lookup"><span data-stu-id="a30cb-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="a30cb-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="a30cb-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="a30cb-121">2つのデータベース間で変更を同期する方向を示す<strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong>定数です。</span><span class="sxs-lookup"><span data-stu-id="a30cb-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a30cb-122">注釈</span><span class="sxs-lookup"><span data-stu-id="a30cb-122">Remarks</span></span>

<span data-ttu-id="a30cb-123">You use **Synchronize** to exchange data and design changes between two databases.</span><span class="sxs-lookup"><span data-stu-id="a30cb-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="a30cb-124">Design changes always happen first.</span><span class="sxs-lookup"><span data-stu-id="a30cb-124">Design changes always happen first.</span></span> <span data-ttu-id="a30cb-125">Both databases must be at the same design level before they can exchange data.</span><span class="sxs-lookup"><span data-stu-id="a30cb-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="a30cb-126">たとえば、データ変更がデータベースから dbpathname にのみフローしているにもかかわらず、 **dbRepExportChanges**型を使用すると、レプリカのデザインが変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a30cb-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="a30cb-127">dbpathname で識別されるレプリカは、同じレプリカセットの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="a30cb-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="a30cb-128">2 つのレプリカの **ReplicaID** プロパティが同じ値に設定されている場合や、2 つのレプリカが異なるレプリカ セットのデザイン マスターである場合、同期化は失敗します。</span><span class="sxs-lookup"><span data-stu-id="a30cb-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="a30cb-129">2 つのレプリカをインターネット経由で同期させる場合は、定数 **dbRepSyncInternet** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a30cb-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="a30cb-130">この場合は、ローカルエリアネットワークパスを指定する代わりに、dbpathname 引数に Uniform resource Locator (URL) アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="a30cb-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="a30cb-131">[!メモ] 部分レプリカを他の部分レプリカに同期させることはできません。</span><span class="sxs-lookup"><span data-stu-id="a30cb-131">You can't synchronize partial replicas with other partial replicas.</span></span> <span data-ttu-id="a30cb-132">詳細については、 [PopulatePartial](database-populatepartial-method-dao.md) メソッドのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a30cb-132">See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


