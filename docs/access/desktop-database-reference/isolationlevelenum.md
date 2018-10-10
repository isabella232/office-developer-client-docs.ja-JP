---
title: IsolationLevelEnum (デスクトップ データベース参照のアクセス)
TOCTitle: IsolationLevelEnum
ms:assetid: 438af3f3-65ed-237d-94d8-f3aff6addd3b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249204(v=office.15)
ms:contentKeyID: 48544506
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80e7d22a5152b24894bf746b939f705739d4220d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479551"
---
# <a name="isolationlevelenum"></a><span data-ttu-id="5f9cd-102">IsolationLevelEnum</span><span class="sxs-lookup"><span data-stu-id="5f9cd-102">IsolationLevelEnum</span></span>


<span data-ttu-id="5f9cd-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f9cd-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="5f9cd-104">[Connection](connection-object-ado.md) オブジェクトのトランザクション分離レベルを表します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-104">Specifies the level of transaction isolation for a [Connection](connection-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f9cd-105">定数</span><span class="sxs-lookup"><span data-stu-id="5f9cd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="5f9cd-106">値</span><span class="sxs-lookup"><span data-stu-id="5f9cd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="5f9cd-107">説明</span><span class="sxs-lookup"><span data-stu-id="5f9cd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-108"><strong>adXactUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-108"><strong>adXactUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-109">-1</span><span class="sxs-lookup"><span data-stu-id="5f9cd-109">-1</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-110">プロバイダーで指定以外の分離レベルが使われているが、そのレベルを判別できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-110">Indicates that the provider is using a different isolation level than specified, but that the level cannot be determined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-111"><strong>adXactChaos</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-111"><strong>adXactChaos</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-112">16</span><span class="sxs-lookup"><span data-stu-id="5f9cd-112">16</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-113">分離レベルが上位のトランザクションによる保留中の変更を上書きできないことを示します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-113">Indicates that pending changes from more highly isolated transactions cannot be overwritten.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-114"><strong>adXactBrowse</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-114"><strong>adXactBrowse</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-115">256</span><span class="sxs-lookup"><span data-stu-id="5f9cd-115">256</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-116">1 つのトランザクションから、他のトランザクションでコミットされていない変更を参照できることを示します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-116">Indicates that from one transaction you can view uncommitted changes in other transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-117"><strong>adXactReadUncommitted</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-117"><strong>adXactReadUncommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-118">256</span><span class="sxs-lookup"><span data-stu-id="5f9cd-118">256</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-119"><strong>adXactBrowse</strong> と同じです。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-119">Same as <strong>adXactBrowse</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-120"><strong>adXactCursorStability</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-120"><strong>adXactCursorStability</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-121">4096</span><span class="sxs-lookup"><span data-stu-id="5f9cd-121">4096</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-122">1 つのトランザクションから、他のトランザクションで行われた変更を参照できるが、参照できるのはその変更のコミット後であることを示します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-122">Indicates that from one transaction you can view changes in other transactions only after they have been committed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-123"><strong>adXactReadCommitted</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-123"><strong>adXactReadCommitted</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-124">4096</span><span class="sxs-lookup"><span data-stu-id="5f9cd-124">4096</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-125"><strong>adXactCursorStability</strong> と同じです。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-125">Same as <strong>adXactCursorStability</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-126"><strong>adXactRepeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-126"><strong>adXactRepeatableRead</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-127">65536</span><span class="sxs-lookup"><span data-stu-id="5f9cd-127">65536</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-128">1 つのトランザクションから、他のトランザクションで行われた変更を参照できないが、再クエリで新規 <strong>Recordset</strong> オブジェクトを取得できることを示します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-128">Indicates that from one transaction you cannot see changes made in other transactions, but that requerying can retrieve new <strong>Recordset</strong> objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-129"><strong>adXactIsolated</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-129"><strong>adXactIsolated</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-130">1048576</span><span class="sxs-lookup"><span data-stu-id="5f9cd-130">1048576</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-131">他のトランザクションとは分離した状態でトランザクションが実行されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-131">Indicates that transactions are conducted in isolation of other transactions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-132"><strong>adXactSerializable</strong></span><span class="sxs-lookup"><span data-stu-id="5f9cd-132"><strong>adXactSerializable</strong></span></span></p></td>
<td><p><span data-ttu-id="5f9cd-133">1048576</span><span class="sxs-lookup"><span data-stu-id="5f9cd-133">1048576</span></span></p></td>
<td><p><span data-ttu-id="5f9cd-134"><strong>adXactIsolated</strong> と同じです。</span><span class="sxs-lookup"><span data-stu-id="5f9cd-134">Same as <strong>adXactIsolated</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5f9cd-135">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="5f9cd-135">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="5f9cd-136">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="5f9cd-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f9cd-137">定数</span><span class="sxs-lookup"><span data-stu-id="5f9cd-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-138">AdoEnums.IsolationLevel.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="5f9cd-138">AdoEnums.IsolationLevel.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-139">AdoEnums.IsolationLevel.CHAOS</span><span class="sxs-lookup"><span data-stu-id="5f9cd-139">AdoEnums.IsolationLevel.CHAOS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-140">AdoEnums.IsolationLevel.BROWSE</span><span class="sxs-lookup"><span data-stu-id="5f9cd-140">AdoEnums.IsolationLevel.BROWSE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="5f9cd-141">AdoEnums.IsolationLevel.READUNCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span><span class="sxs-lookup"><span data-stu-id="5f9cd-142">AdoEnums.IsolationLevel.CURSORSTABILITY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-143">AdoEnums.IsolationLevel.READCOMMITTED</span><span class="sxs-lookup"><span data-stu-id="5f9cd-143">AdoEnums.IsolationLevel.READCOMMITTED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span><span class="sxs-lookup"><span data-stu-id="5f9cd-144">AdoEnums.IsolationLevel.REPEATABLEREAD</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f9cd-145">AdoEnums.IsolationLevel.ISOLATED</span><span class="sxs-lookup"><span data-stu-id="5f9cd-145">AdoEnums.IsolationLevel.ISOLATED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f9cd-146">AdoEnums.IsolationLevel.SERIALIZABLE</span><span class="sxs-lookup"><span data-stu-id="5f9cd-146">AdoEnums.IsolationLevel.SERIALIZABLE</span></span></p></td>
</tr>
</tbody>
</table>

