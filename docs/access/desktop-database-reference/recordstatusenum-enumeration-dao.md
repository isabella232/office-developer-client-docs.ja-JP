---
title: RecordStatusEnum 列挙 (DAO)
TOCTitle: RecordStatusEnum Enumeration
ms:assetid: bf4492f2-8d8f-f10f-7a3c-d6296d2ce96b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822784(v=office.15)
ms:contentKeyID: 48547483
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78f86e8c80a6bbc09499e9512e2daee87fc67998
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477241"
---
# <a name="recordstatusenum-enumeration-dao"></a><span data-ttu-id="38ada-102">RecordStatusEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="38ada-102">RecordStatusEnum Enumeration (DAO)</span></span>


<span data-ttu-id="38ada-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="38ada-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="38ada-104">**RecordStatus** プロパティで、一括更新の場合の現在のレコードの更新状態を示すために使用します。</span><span class="sxs-lookup"><span data-stu-id="38ada-104">Used with the **RecordStatus** property to indicate the update status of the current record if it is part of a batch update.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38ada-105">名前</span><span class="sxs-lookup"><span data-stu-id="38ada-105">Name</span></span></p></th>
<th><p><span data-ttu-id="38ada-106">値</span><span class="sxs-lookup"><span data-stu-id="38ada-106">Value</span></span></p></th>
<th><p><span data-ttu-id="38ada-107">説明</span><span class="sxs-lookup"><span data-stu-id="38ada-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38ada-108">dbRecordDBDeleted</span><span class="sxs-lookup"><span data-stu-id="38ada-108">dbRecordDBDeleted</span></span></p></td>
<td><p><span data-ttu-id="38ada-109">4</span><span class="sxs-lookup"><span data-stu-id="38ada-109">4</span></span></p></td>
<td><p><span data-ttu-id="38ada-110">レコードはローカルで削除され、データベース内でも削除されました。</span><span class="sxs-lookup"><span data-stu-id="38ada-110">The record has been deleted locally and in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38ada-111">dbRecordDeleted</span><span class="sxs-lookup"><span data-stu-id="38ada-111">dbRecordDeleted</span></span></p></td>
<td><p><span data-ttu-id="38ada-112">3</span><span class="sxs-lookup"><span data-stu-id="38ada-112">3</span></span></p></td>
<td><p><span data-ttu-id="38ada-113">レコードは削除されましたが、データベース内ではまだ削除されていません。</span><span class="sxs-lookup"><span data-stu-id="38ada-113">The record has been deleted, but not yet deleted in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38ada-114">dbRecordModified</span><span class="sxs-lookup"><span data-stu-id="38ada-114">dbRecordModified</span></span></p></td>
<td><p><span data-ttu-id="38ada-115">1</span><span class="sxs-lookup"><span data-stu-id="38ada-115">1</span></span></p></td>
<td><p><span data-ttu-id="38ada-116">レコードは変更されましたが、データベース内では更新されていません。</span><span class="sxs-lookup"><span data-stu-id="38ada-116">The record has been modified and not updated in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38ada-117">dbRecordNew</span><span class="sxs-lookup"><span data-stu-id="38ada-117">dbRecordNew</span></span></p></td>
<td><p><span data-ttu-id="38ada-118">2</span><span class="sxs-lookup"><span data-stu-id="38ada-118">2</span></span></p></td>
<td><p><span data-ttu-id="38ada-119">レコードは <strong>AddNew</strong> メソッドによって挿入されましたが、データベースにはまだ挿入されていません。</span><span class="sxs-lookup"><span data-stu-id="38ada-119">The record has been inserted with the <strong>AddNew</strong> method, but not yet inserted into the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38ada-120">dbRecordUnmodified</span><span class="sxs-lookup"><span data-stu-id="38ada-120">dbRecordUnmodified</span></span></p></td>
<td><p><span data-ttu-id="38ada-121">0</span><span class="sxs-lookup"><span data-stu-id="38ada-121">0</span></span></p></td>
<td><p><span data-ttu-id="38ada-122">(既定値) レコードはまだ変更されていないか、正しく更新されました。</span><span class="sxs-lookup"><span data-stu-id="38ada-122">(Default) The record has not been modified or has been updated successfully.</span></span></p></td>
</tr>
</tbody>
</table>

