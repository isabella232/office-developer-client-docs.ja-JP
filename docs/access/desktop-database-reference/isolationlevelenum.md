---
title: IsolationLevelEnum (デスクトップ データベース参照のアクセス)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 7e32cd3c8ae78199f90fcac8cccdf377bf332d38
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863942"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="5c3c7-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="5c3c7-102">IsolationLevelEnum</span></span>

<span data-ttu-id="5c3c7-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5c3c7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5c3c7-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション分離レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c3c7-105">定数</span><span class="sxs-lookup"><span data-stu-id="5c3c7-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5c3c7-106">値</span><span class="sxs-lookup"><span data-stu-id="5c3c7-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5c3c7-107">説明</span><span class="sxs-lookup"><span data-stu-id="5c3c7-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-109">-1</span><span class="sxs-lookup"><span data-stu-id="5c3c7-109">-1</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-110">プロバイダーで指定以外の分離レベルが使われているが、そのレベルを判別できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-112">16</span><span class="sxs-lookup"><span data-stu-id="5c3c7-112">16</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-113">分離レベルが上位のトランザクションによる保留中の変更を上書きできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-115">256</span><span class="sxs-lookup"><span data-stu-id="5c3c7-115">256</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-116">1 つのトランザクションから、他のトランザクションでコミットされていない変更を参照できることを示します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-118">256</span><span class="sxs-lookup"><span data-stu-id="5c3c7-118">256</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-119"><strong>adXactBrowse</strong> と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-121">4096</span><span class="sxs-lookup"><span data-stu-id="5c3c7-121">4096</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-122">1 つのトランザクションから、他のトランザクションで行われた変更を参照できるが、参照できるのはその変更のコミット後であることを示します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-124">4096</span><span class="sxs-lookup"><span data-stu-id="5c3c7-124">4096</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-125"><strong>adXactCursorStability</strong> と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-127">65536</span><span class="sxs-lookup"><span data-stu-id="5c3c7-127">65536</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-128">1 つのトランザクションから、他のトランザクションで行われた変更を参照できないが、再クエリで新規 <strong>Recordset</strong> オブジェクトを取得できることを示します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-130">1048576</span><span class="sxs-lookup"><span data-stu-id="5c3c7-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-131">他のトランザクションとは分離した状態でトランザクションが実行されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="5c3c7-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="5c3c7-133">1048576</span><span class="sxs-lookup"><span data-stu-id="5c3c7-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="5c3c7-134"><strong>adXactIsolated</strong> と同じです。</span><span class="sxs-lookup"><span data-stu-id="5c3c7-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="5c3c7-135">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="5c3c7-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="5c3c7-136">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5c3c7-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5c3c7-137">定数</span><span class="sxs-lookup"><span data-stu-id="5c3c7-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="5c3c7-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="5c3c7-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="5c3c7-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="5c3c7-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="5c3c7-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="5c3c7-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="5c3c7-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c3c7-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="5c3c7-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c3c7-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="5c3c7-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

