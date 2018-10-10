---
title: SeekEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6a151f7a4549a234c20f76bc1ac93d5eff6cf250
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476209"
---
# <a name="seekenum"></a><span data-ttu-id="33704-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="33704-102">SeekEnum</span></span>


<span data-ttu-id="33704-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="33704-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33704-104">実行する [Seek](seek-method-ado.md) の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="33704-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33704-105">定数</span><span class="sxs-lookup"><span data-stu-id="33704-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="33704-106">値</span><span class="sxs-lookup"><span data-stu-id="33704-106">Value</span></span></p></th>
<th><p><span data-ttu-id="33704-107">説明</span><span class="sxs-lookup"><span data-stu-id="33704-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33704-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="33704-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="33704-109">1</span><span class="sxs-lookup"><span data-stu-id="33704-109">1</span></span></p></td>
<td><p><span data-ttu-id="33704-110"><em>KeyValues</em> と一致する最初のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="33704-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33704-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="33704-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="33704-112">2</span><span class="sxs-lookup"><span data-stu-id="33704-112">2</span></span></p></td>
<td><p><span data-ttu-id="33704-113"><em>KeyValues</em> と一致する最後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="33704-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33704-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="33704-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="33704-115">4</span><span class="sxs-lookup"><span data-stu-id="33704-115">4</span></span></p></td>
<td><p><span data-ttu-id="33704-116"><em>KeyValues</em> と一致するキー、またはその直後のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="33704-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33704-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="33704-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="33704-118">8</span><span class="sxs-lookup"><span data-stu-id="33704-118">8</span></span></p></td>
<td><p><span data-ttu-id="33704-119"><em>KeyValues</em> と一致するキーの直後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="33704-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33704-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="33704-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="33704-121">16</span><span class="sxs-lookup"><span data-stu-id="33704-121">16</span></span></p></td>
<td><p><span data-ttu-id="33704-122"><em>KeyValues</em> と一致するキー、またはその直前のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="33704-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33704-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="33704-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="33704-124">32</span><span class="sxs-lookup"><span data-stu-id="33704-124">32</span></span></p></td>
<td><p><span data-ttu-id="33704-125"><em>KeyValues</em> と一致するキーの直前のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="33704-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="33704-126">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="33704-126">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="33704-127">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="33704-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="33704-128">定数</span><span class="sxs-lookup"><span data-stu-id="33704-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="33704-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="33704-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33704-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="33704-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33704-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="33704-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33704-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="33704-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="33704-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="33704-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="33704-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="33704-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

