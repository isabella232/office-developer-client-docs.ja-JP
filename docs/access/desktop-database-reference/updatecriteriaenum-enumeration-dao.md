---
title: UpdateCriteriaEnum 列挙 (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b8035d90da62f83c930a208cac73f1fe45d61340
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880496"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="9cc63-102">UpdateCriteriaEnum 列挙 (DAO)</span><span class="sxs-lookup"><span data-stu-id="9cc63-102">UpdateCriteriaEnum Enumeration (DAO)</span></span>


<span data-ttu-id="9cc63-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9cc63-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9cc63-104">**UpdateOptions** メソッドで、一括更新の構築方法を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="9cc63-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9cc63-105">名前</span><span class="sxs-lookup"><span data-stu-id="9cc63-105">Name</span></span></p></th>
<th><p><span data-ttu-id="9cc63-106">値</span><span class="sxs-lookup"><span data-stu-id="9cc63-106">Value</span></span></p></th>
<th><p><span data-ttu-id="9cc63-107">説明</span><span class="sxs-lookup"><span data-stu-id="9cc63-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9cc63-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="9cc63-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="9cc63-109">4</span><span class="sxs-lookup"><span data-stu-id="9cc63-109">4</span></span></p></td>
<td><p><span data-ttu-id="9cc63-110">キー列 (1 つまたは複数) とすべての列を where 句で使用します。</span><span class="sxs-lookup"><span data-stu-id="9cc63-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc63-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="9cc63-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="9cc63-112">16</span><span class="sxs-lookup"><span data-stu-id="9cc63-112">16</span></span></p></td>
<td><p><span data-ttu-id="9cc63-113">変更された行ごとに、DELETE ステートメントと INSERT ステートメントのペアを使用します。</span><span class="sxs-lookup"><span data-stu-id="9cc63-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc63-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="9cc63-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="9cc63-115">1</span><span class="sxs-lookup"><span data-stu-id="9cc63-115">1</span></span></p></td>
<td><p><span data-ttu-id="9cc63-116">キー列 (1 つまたは複数) のみを where 句で使用します。</span><span class="sxs-lookup"><span data-stu-id="9cc63-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc63-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="9cc63-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="9cc63-118">2</span><span class="sxs-lookup"><span data-stu-id="9cc63-118">2</span></span></p></td>
<td><p><span data-ttu-id="9cc63-119">キー列 (1 つまたは複数) と更新されたすべての列を where 句で使用します。</span><span class="sxs-lookup"><span data-stu-id="9cc63-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9cc63-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="9cc63-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="9cc63-121">8</span><span class="sxs-lookup"><span data-stu-id="9cc63-121">8</span></span></p></td>
<td><p><span data-ttu-id="9cc63-122">タイムスタンプ列が使用可能な場合、タイムスタンプ列のみを使用します (結果セットにタイムスタンプ列が含まれない場合は、実行時エラーを生成します)。</span><span class="sxs-lookup"><span data-stu-id="9cc63-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9cc63-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="9cc63-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="9cc63-124">32</span><span class="sxs-lookup"><span data-stu-id="9cc63-124">32</span></span></p></td>
<td><p><span data-ttu-id="9cc63-125">変更された行ごとに UPDATE ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="9cc63-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

