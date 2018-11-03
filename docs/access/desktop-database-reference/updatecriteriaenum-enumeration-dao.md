---
title: UpdateCriteriaEnum 列挙型 (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6160c53dd1cab26b2b92ec023f28158635d7081
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944467"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="118e9-102">UpdateCriteriaEnum 列挙型 (DAO)</span><span class="sxs-lookup"><span data-stu-id="118e9-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="118e9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="118e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="118e9-104">**UpdateOptions** メソッドで、一括更新の構築方法を指定するために使用します。</span><span class="sxs-lookup"><span data-stu-id="118e9-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="118e9-105">名前</span><span class="sxs-lookup"><span data-stu-id="118e9-105">Name</span></span></p></th>
<th><p><span data-ttu-id="118e9-106">値</span><span class="sxs-lookup"><span data-stu-id="118e9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="118e9-107">説明</span><span class="sxs-lookup"><span data-stu-id="118e9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="118e9-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="118e9-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="118e9-109">4</span><span class="sxs-lookup"><span data-stu-id="118e9-109">4</span></span></p></td>
<td><p><span data-ttu-id="118e9-110">キー列 (1 つまたは複数) とすべての列を where 句で使用します。</span><span class="sxs-lookup"><span data-stu-id="118e9-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118e9-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="118e9-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="118e9-112">16</span><span class="sxs-lookup"><span data-stu-id="118e9-112">16</span></span></p></td>
<td><p><span data-ttu-id="118e9-113">変更された行ごとに、DELETE ステートメントと INSERT ステートメントのペアを使用します。</span><span class="sxs-lookup"><span data-stu-id="118e9-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="118e9-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="118e9-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="118e9-115">1</span><span class="sxs-lookup"><span data-stu-id="118e9-115">1</span></span></p></td>
<td><p><span data-ttu-id="118e9-116">キー列 (1 つまたは複数) のみを where 句で使用します。</span><span class="sxs-lookup"><span data-stu-id="118e9-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118e9-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="118e9-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="118e9-118">2</span><span class="sxs-lookup"><span data-stu-id="118e9-118">2</span></span></p></td>
<td><p><span data-ttu-id="118e9-119">キー列 (1 つまたは複数) と更新されたすべての列を where 句で使用します。</span><span class="sxs-lookup"><span data-stu-id="118e9-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="118e9-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="118e9-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="118e9-121">8</span><span class="sxs-lookup"><span data-stu-id="118e9-121">8</span></span></p></td>
<td><p><span data-ttu-id="118e9-122">タイムスタンプ列が使用可能な場合、タイムスタンプ列のみを使用します (結果セットにタイムスタンプ列が含まれない場合は、実行時エラーを生成します)。</span><span class="sxs-lookup"><span data-stu-id="118e9-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="118e9-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="118e9-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="118e9-124">32</span><span class="sxs-lookup"><span data-stu-id="118e9-124">32</span></span></p></td>
<td><p><span data-ttu-id="118e9-125">変更された行ごとに UPDATE ステートメントを使用します。</span><span class="sxs-lookup"><span data-stu-id="118e9-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

