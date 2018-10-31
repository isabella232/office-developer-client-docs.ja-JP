---
title: FilterGroupEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FilterGroupEnum
ms:assetid: 141f8f9a-c188-5937-91cc-3155eaebebd2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248912(v=office.15)
ms:contentKeyID: 48543381
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: fc2c41ddd672ff303584762f6091bab4c128de99
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862696"
---
# <a name="filtergroupenum"></a><span data-ttu-id="cef6a-102">FilterGroupEnum</span><span class="sxs-lookup"><span data-stu-id="cef6a-102">FilterGroupEnum</span></span>

<span data-ttu-id="cef6a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="cef6a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="cef6a-104">[Recordset](recordset-object-ado.md) でフィルターの対象となるレコード グループを表します。</span><span class="sxs-lookup"><span data-stu-id="cef6a-104">Specifies the group of records to be filtered from a [Recordset](recordset-object-ado.md).</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cef6a-105">定数</span><span class="sxs-lookup"><span data-stu-id="cef6a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cef6a-106">値</span><span class="sxs-lookup"><span data-stu-id="cef6a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cef6a-107">説明</span><span class="sxs-lookup"><span data-stu-id="cef6a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cef6a-108"><strong>adFilterAffectedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="cef6a-108"><strong>adFilterAffectedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="cef6a-109">2</span><span class="sxs-lookup"><span data-stu-id="cef6a-109">2</span></span></p></td>
<td><p><span data-ttu-id="cef6a-110">最後に行った <a href="delete-method-ado-recordset.md">Delete</a>、<a href="resync-method-ado.md">Resync</a>、<a href="updatebatch-method-ado.md">UpdateBatch</a>、または <a href="cancelbatch-method-ado.md">CancelBatch</a> 呼び出しで影響を受けたレコードのみを表示するようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="cef6a-110">Filters for viewing only records affected by the last <a href="delete-method-ado-recordset.md">Delete</a>, <a href="resync-method-ado.md">Resync</a>, <a href="updatebatch-method-ado.md">UpdateBatch</a>, or <a href="cancelbatch-method-ado.md">CancelBatch</a> call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cef6a-111"><strong>競合</strong></span><span class="sxs-lookup"><span data-stu-id="cef6a-111"><strong>adFilterConflictingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="cef6a-112">5</span><span class="sxs-lookup"><span data-stu-id="cef6a-112">5</span></span></p></td>
<td><p><span data-ttu-id="cef6a-113">最後に行ったバッチ更新が失敗したレコードを表示するようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="cef6a-113">Filters for viewing the records that failed the last batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cef6a-114"><strong>adFilterFetchedRecords</strong></span><span class="sxs-lookup"><span data-stu-id="cef6a-114"><strong>adFilterFetchedRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="cef6a-115">3</span><span class="sxs-lookup"><span data-stu-id="cef6a-115">3</span></span></p></td>
<td><p><span data-ttu-id="cef6a-116">データベースから最後に取得されたレコードである現在のキャッシュ内のレコードを表示するようにフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="cef6a-116">Filters for viewing the records in the current cache — that is, the results of the last call to retrieve records from the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cef6a-117"><strong>adFilterNone</strong></span><span class="sxs-lookup"><span data-stu-id="cef6a-117"><strong>adFilterNone</strong></span></span></p></td>
<td><p><span data-ttu-id="cef6a-118">0</span><span class="sxs-lookup"><span data-stu-id="cef6a-118">0</span></span></p></td>
<td><p><span data-ttu-id="cef6a-119">現在のフィルターを削除し、すべてのレコードを復元して表示します。</span><span class="sxs-lookup"><span data-stu-id="cef6a-119">Removes the current filter and restores all records for viewing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cef6a-120"><strong>行と列</strong></span><span class="sxs-lookup"><span data-stu-id="cef6a-120"><strong>adFilterPendingRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="cef6a-121">1</span><span class="sxs-lookup"><span data-stu-id="cef6a-121">1</span></span></p></td>
<td><p><span data-ttu-id="cef6a-p101">変更が行われたが、変更内容がサーバーにまだ送信されていないレコードのみを表示するようにフィルター処理します。バッチ更新モードの場合のみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="cef6a-p101">Filters for viewing only records that have changed but have not yet been sent to the server. Applicable only for batch update mode.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cef6a-124">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="cef6a-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="cef6a-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cef6a-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cef6a-126">定数</span><span class="sxs-lookup"><span data-stu-id="cef6a-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cef6a-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="cef6a-127">AdoEnums.FilterGroup.AFFECTEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cef6a-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="cef6a-128">AdoEnums.FilterGroup.CONFLICTINGRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cef6a-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span><span class="sxs-lookup"><span data-stu-id="cef6a-129">AdoEnums.FilterGroup.FETCHEDRECORDS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cef6a-130">AdoEnums.FilterGroup.NONE</span><span class="sxs-lookup"><span data-stu-id="cef6a-130">AdoEnums.FilterGroup.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cef6a-131">AdoEnums.FilterGroup.PENDINGRECORDS</span><span class="sxs-lookup"><span data-stu-id="cef6a-131">AdoEnums.FilterGroup.PENDINGRECORDS</span></span></p></td>
</tr>
</tbody>
</table>

