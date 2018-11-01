---
title: SeekEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5035853f8896b711687fed9f9651af6665d9d9b6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875722"
---
# <a name="seekenum"></a><span data-ttu-id="03ea0-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="03ea0-102">SeekEnum</span></span>

<span data-ttu-id="03ea0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="03ea0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="03ea0-104">実行する [Seek](seek-method-ado.md) の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03ea0-105">定数</span><span class="sxs-lookup"><span data-stu-id="03ea0-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="03ea0-106">値</span><span class="sxs-lookup"><span data-stu-id="03ea0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="03ea0-107">説明</span><span class="sxs-lookup"><span data-stu-id="03ea0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03ea0-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="03ea0-109">1</span><span class="sxs-lookup"><span data-stu-id="03ea0-109">1</span></span></p></td>
<td><p><span data-ttu-id="03ea0-110"><em>KeyValues</em> と一致する最初のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ea0-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="03ea0-112">2</span><span class="sxs-lookup"><span data-stu-id="03ea0-112">2</span></span></p></td>
<td><p><span data-ttu-id="03ea0-113"><em>KeyValues</em> と一致する最後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ea0-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="03ea0-115">4</span><span class="sxs-lookup"><span data-stu-id="03ea0-115">4</span></span></p></td>
<td><p><span data-ttu-id="03ea0-116"><em>KeyValues</em> と一致するキー、またはその直後のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ea0-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="03ea0-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="03ea0-118">8</span><span class="sxs-lookup"><span data-stu-id="03ea0-118">8</span></span></p></td>
<td><p><span data-ttu-id="03ea0-119"><em>KeyValues</em> と一致するキーの直後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ea0-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="03ea0-121">16</span><span class="sxs-lookup"><span data-stu-id="03ea0-121">16</span></span></p></td>
<td><p><span data-ttu-id="03ea0-122"><em>KeyValues</em> と一致するキー、またはその直前のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ea0-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="03ea0-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="03ea0-124">32</span><span class="sxs-lookup"><span data-stu-id="03ea0-124">32</span></span></p></td>
<td><p><span data-ttu-id="03ea0-125"><em>KeyValues</em> と一致するキーの直前のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="03ea0-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="03ea0-126">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="03ea0-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="03ea0-127">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="03ea0-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="03ea0-128">定数</span><span class="sxs-lookup"><span data-stu-id="03ea0-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03ea0-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ea0-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ea0-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ea0-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="03ea0-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03ea0-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="03ea0-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03ea0-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="03ea0-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

