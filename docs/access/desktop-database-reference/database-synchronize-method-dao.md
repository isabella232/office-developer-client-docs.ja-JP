---
title: Database.Synchronize メソッド (DAO)
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
ms.openlocfilehash: b25536c158c248695c9e537a0153922b2518058a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863291"
---
# <a name="databasesynchronize-method-dao"></a><span data-ttu-id="30ed8-102">Database.Synchronize メソッド (DAO)</span><span class="sxs-lookup"><span data-stu-id="30ed8-102">Database.Synchronize Method (DAO)</span></span>


<span data-ttu-id="30ed8-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="30ed8-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="30ed8-p101">2 つのレプリカの同期をとります (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="30ed8-p101">Synchronizes two replicas. (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="30ed8-106">構文</span><span class="sxs-lookup"><span data-stu-id="30ed8-106">Syntax</span></span>

<span data-ttu-id="30ed8-107">*式*です。(***DbPathName***、 ***ExchangeType***) を同期します。</span><span class="sxs-lookup"><span data-stu-id="30ed8-107">*expression* .Synchronize(***DbPathName***, ***ExchangeType***)</span></span>

<span data-ttu-id="30ed8-108">\*式\***データベース**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="30ed8-108">*expression* A variable that represents a **Database** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="30ed8-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="30ed8-109">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30ed8-110">名前</span><span class="sxs-lookup"><span data-stu-id="30ed8-110">Name</span></span></p></th>
<th><p><span data-ttu-id="30ed8-111">必須/オプション</span><span class="sxs-lookup"><span data-stu-id="30ed8-111">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="30ed8-112">データ型</span><span class="sxs-lookup"><span data-stu-id="30ed8-112">Data Type</span></span></p></th>
<th><p><span data-ttu-id="30ed8-113">説明</span><span class="sxs-lookup"><span data-stu-id="30ed8-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30ed8-114">DbPathName</span><span class="sxs-lookup"><span data-stu-id="30ed8-114">DbPathName</span></span></p></td>
<td><p><span data-ttu-id="30ed8-115">必須</span><span class="sxs-lookup"><span data-stu-id="30ed8-115">Required</span></span></p></td>
<td><p><span data-ttu-id="30ed8-116"><strong>文字列型 (String)</strong></span><span class="sxs-lookup"><span data-stu-id="30ed8-116"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="30ed8-117">データベースを同期させる対象のレプリカへのパスです。</span><span class="sxs-lookup"><span data-stu-id="30ed8-117">The path to the target replica with which database will be synchronized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30ed8-118">ExchangeType</span><span class="sxs-lookup"><span data-stu-id="30ed8-118">ExchangeType</span></span></p></td>
<td><p><span data-ttu-id="30ed8-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="30ed8-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="30ed8-120"><strong>バリアント型 (Variant)</strong></span><span class="sxs-lookup"><span data-stu-id="30ed8-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="30ed8-121">2 つのデータベース間で変更を同期させる方向を示す <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> クラスの定数です。</span><span class="sxs-lookup"><span data-stu-id="30ed8-121">A <strong><a href="synchronizetypeenum-enumeration-dao.md">SynchronizeTypeEnum</a></strong> constant indicating which direction to synchronize changes between the two databases.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="30ed8-122">注釈</span><span class="sxs-lookup"><span data-stu-id="30ed8-122">Remarks</span></span>

<span data-ttu-id="30ed8-123">2 つのデータベース間でデータおよびデザインの変更内容を交換するのにには、**同期**を使用します。</span><span class="sxs-lookup"><span data-stu-id="30ed8-123">You use **Synchronize** to exchange data and design changes between two databases.</span></span> <span data-ttu-id="30ed8-124">デザインの変更は、常に最初に発生します。</span><span class="sxs-lookup"><span data-stu-id="30ed8-124">Design changes always happen first.</span></span> <span data-ttu-id="30ed8-125">両方のデータベースする必要があります同じデザイン レベルで交換するにはデータです。</span><span class="sxs-lookup"><span data-stu-id="30ed8-125">Both databases must be at the same design level before they can exchange data.</span></span> <span data-ttu-id="30ed8-126">などの種類が**dbRepExportChanges**の交換可能性があります、レプリカでデザインの変更データのみ、データベースから DbPathName にフローを変更する場合でも。</span><span class="sxs-lookup"><span data-stu-id="30ed8-126">For example, an exchange of type **dbRepExportChanges** might cause design changes at a replica even though data changes flow only from the database to DbPathName.</span></span>

<span data-ttu-id="30ed8-127">DbPathName で識別されるレプリカは、同じレプリカ セットの一部である必要があります。</span><span class="sxs-lookup"><span data-stu-id="30ed8-127">The replica identified in DbPathName must be part of the same replica set.</span></span> <span data-ttu-id="30ed8-128">2 つのレプリカの **ReplicaID** プロパティが同じ値に設定されている場合や、2 つのレプリカが異なるレプリカ セットのデザイン マスターである場合、同期化は失敗します。</span><span class="sxs-lookup"><span data-stu-id="30ed8-128">If both replicas have the same **ReplicaID** property setting or are Design Masters for two different replica sets, the synchronization fails.</span></span>

<span data-ttu-id="30ed8-129">2 つのレプリカをインターネット経由で同期させる場合は、定数 **dbRepSyncInternet** を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="30ed8-129">When you synchronize two replicas over the Internet, you must use the **dbRepSyncInternet** constant.</span></span> <span data-ttu-id="30ed8-130">この例では、ローカル エリア ネットワーク パスを指定するのではなく引数 DbPathName の統一リソース ロケーター (URL) アドレスを指定します。</span><span class="sxs-lookup"><span data-stu-id="30ed8-130">In this case, you specify a Uniform Resource Locator (URL) address for the DbPathName argument instead of specifying a local area network path.</span></span>


> [!NOTE]
> <span data-ttu-id="30ed8-p105">[!メモ] 部分レプリカを他の部分レプリカに同期させることはできません。詳細については、 [PopulatePartial](database-populatepartial-method-dao.md) メソッドのトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="30ed8-p105">You can't synchronize partial replicas with other partial replicas. See the [PopulatePartial](database-populatepartial-method-dao.md) method for more information.</span></span>


