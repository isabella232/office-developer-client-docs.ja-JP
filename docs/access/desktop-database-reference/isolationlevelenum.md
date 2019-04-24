---
title: IsolationLevelEnum (Access デスクトップデータベースリファレンス)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9f0176772b366b39d368f8bae1e402d420f0136c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291157"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="6574d-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="6574d-102">IsolationLevelEnum</span></span>

<span data-ttu-id="6574d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="6574d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6574d-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション分離レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="6574d-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6574d-105">定数</span><span class="sxs-lookup"><span data-stu-id="6574d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6574d-106">値</span><span class="sxs-lookup"><span data-stu-id="6574d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6574d-107">説明</span><span class="sxs-lookup"><span data-stu-id="6574d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6574d-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-109">-1</span><span class="sxs-lookup"><span data-stu-id="6574d-109">-1</span></span></p></td>
<td><p><span data-ttu-id="6574d-110">プロバイダーが指定されたものとは異なる分離レベルを使用していますが、レベルを特定できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6574d-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-112">16</span><span class="sxs-lookup"><span data-stu-id="6574d-112">16</span></span></p></td>
<td><p><span data-ttu-id="6574d-113">分離度の高いトランザクションからの保留中の変更を上書きできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="6574d-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-115">256</span><span class="sxs-lookup"><span data-stu-id="6574d-115">256</span></span></p></td>
<td><p><span data-ttu-id="6574d-116">1つのトランザクションから、他のトランザクションのコミットされていない変更を表示できることを示します。</span><span class="sxs-lookup"><span data-stu-id="6574d-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-118">256</span><span class="sxs-lookup"><span data-stu-id="6574d-118">256</span></span></p></td>
<td><p><span data-ttu-id="6574d-119"><strong>adXactBrowse</strong>と同じです。</span><span class="sxs-lookup"><span data-stu-id="6574d-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-121">4096</span><span class="sxs-lookup"><span data-stu-id="6574d-121">4096</span></span></p></td>
<td><p><span data-ttu-id="6574d-122">1つのトランザクションから、コミットされた後にのみ他のトランザクションの変更を表示できることを示します。</span><span class="sxs-lookup"><span data-stu-id="6574d-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-124">4096</span><span class="sxs-lookup"><span data-stu-id="6574d-124">4096</span></span></p></td>
<td><p><span data-ttu-id="6574d-125"><strong>adXactCursorStability</strong>と同じです。</span><span class="sxs-lookup"><span data-stu-id="6574d-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-127">65536</span><span class="sxs-lookup"><span data-stu-id="6574d-127">65536</span></span></p></td>
<td><p><span data-ttu-id="6574d-128">1つのトランザクションから、他のトランザクションで行われた変更を表示できないが、再クエリで新しい<strong>Recordset</strong>オブジェクトを取得できることを示します。</span><span class="sxs-lookup"><span data-stu-id="6574d-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-130">1048576</span><span class="sxs-lookup"><span data-stu-id="6574d-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="6574d-131">トランザクションが他のトランザクションとは分離して実行されることを示します。</span><span class="sxs-lookup"><span data-stu-id="6574d-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="6574d-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="6574d-133">1048576</span><span class="sxs-lookup"><span data-stu-id="6574d-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="6574d-134"><strong>adXactIsolated</strong>と同じです。</span><span class="sxs-lookup"><span data-stu-id="6574d-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6574d-135">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="6574d-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="6574d-136">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6574d-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6574d-137">定数</span><span class="sxs-lookup"><span data-stu-id="6574d-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6574d-138">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="6574d-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-139">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="6574d-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-140">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="6574d-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-141">AdoEnums IsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6574d-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-142">IsolationLevel の安定性 AdoEnums</span><span class="sxs-lookup"><span data-stu-id="6574d-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-143">AdoEnums コミットされた IsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6574d-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-144">AdoEnums IsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6574d-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6574d-145">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="6574d-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6574d-146">AdoEnums IsolationLevel</span><span class="sxs-lookup"><span data-stu-id="6574d-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

