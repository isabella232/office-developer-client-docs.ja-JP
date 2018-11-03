---
title: 可能列挙 (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 662176616b267e2fe60b225a3d3def7418e7bcaf
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944355"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="0a5b6-102">可能列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="0a5b6-102">RecordStatusEnum enumeration (DAO)</span></span>


<span data-ttu-id="0a5b6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a5b6-104">**RecordStatus** プロパティで、一括更新の場合の現在のレコードの更新状態を示すために使用します。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0a5b6-105">名前</span><span class="sxs-lookup"><span data-stu-id="0a5b6-105">Name</span></span></p></th>
<th><p><span data-ttu-id="0a5b6-106">値</span><span class="sxs-lookup"><span data-stu-id="0a5b6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="0a5b6-107">説明</span><span class="sxs-lookup"><span data-stu-id="0a5b6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0a5b6-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="0a5b6-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-109">4</span><span class="sxs-lookup"><span data-stu-id="0a5b6-109">4</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-110">レコードはローカルで削除され、データベース内でも削除されました。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a5b6-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="0a5b6-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-112">3</span><span class="sxs-lookup"><span data-stu-id="0a5b6-112">3</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-113">レコードは削除されましたが、データベース内ではまだ削除されていません。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a5b6-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="0a5b6-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-115">1</span><span class="sxs-lookup"><span data-stu-id="0a5b6-115">1</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-116">レコードは変更されましたが、データベース内では更新されていません。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0a5b6-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="0a5b6-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-118">2</span><span class="sxs-lookup"><span data-stu-id="0a5b6-118">2</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-119">レコードは <strong>AddNew</strong> メソッドによって挿入されましたが、データベースにはまだ挿入されていません。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0a5b6-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="0a5b6-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-121">0</span><span class="sxs-lookup"><span data-stu-id="0a5b6-121">0</span></span></p></td>
<td><p><span data-ttu-id="0a5b6-122">(既定値) レコードはまだ変更されていないか、正しく更新されました。</span><span class="sxs-lookup"><span data-stu-id="0a5b6-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

