---
title: SeekEnum (デスクトップ データベース参照のアクセス)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 5025706d64927482b632a17a5f71839cd4186619
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861415"
---
# <a name="seekenum"></a><span data-ttu-id="41e56-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="41e56-102">SeekEnum</span></span>

<span data-ttu-id="41e56-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="41e56-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="41e56-104">実行する [Seek](seek-method-ado.md) の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="41e56-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41e56-105">定数</span><span class="sxs-lookup"><span data-stu-id="41e56-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="41e56-106">値</span><span class="sxs-lookup"><span data-stu-id="41e56-106">Value</span></span></p></th>
<th><p><span data-ttu-id="41e56-107">説明</span><span class="sxs-lookup"><span data-stu-id="41e56-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41e56-108">adSeekFirstEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="41e56-109">1</span><span class="sxs-lookup"><span data-stu-id="41e56-109">1</span></span></p></td>
<td><p><span data-ttu-id="41e56-110"><em>KeyValues</em> と一致する最初のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="41e56-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e56-111">adSeekLastEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="41e56-112">2</span><span class="sxs-lookup"><span data-stu-id="41e56-112">2</span></span></p></td>
<td><p><span data-ttu-id="41e56-113"><em>KeyValues</em> と一致する最後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="41e56-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41e56-114">adSeekAfterEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="41e56-115">4</span><span class="sxs-lookup"><span data-stu-id="41e56-115">4</span></span></p></td>
<td><p><span data-ttu-id="41e56-116"><em>KeyValues</em> と一致するキー、またはその直後のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="41e56-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e56-117">adSeekAfter</span><span class="sxs-lookup"><span data-stu-id="41e56-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="41e56-118">8</span><span class="sxs-lookup"><span data-stu-id="41e56-118">8</span></span></p></td>
<td><p><span data-ttu-id="41e56-119"><em>KeyValues</em> と一致するキーの直後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="41e56-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41e56-120">adSeekBeforeEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="41e56-121">16</span><span class="sxs-lookup"><span data-stu-id="41e56-121">16</span></span></p></td>
<td><p><span data-ttu-id="41e56-122"><em>KeyValues</em> と一致するキー、またはその直前のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="41e56-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e56-123">adSeekBefore</span><span class="sxs-lookup"><span data-stu-id="41e56-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="41e56-124">32</span><span class="sxs-lookup"><span data-stu-id="41e56-124">32</span></span></p></td>
<td><p><span data-ttu-id="41e56-125"><em>KeyValues</em> と一致するキーの直前のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="41e56-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="41e56-126">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="41e56-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="41e56-127">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="41e56-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41e56-128">定数</span><span class="sxs-lookup"><span data-stu-id="41e56-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41e56-129">AdoEnums.Seek.FIRSTEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e56-130">AdoEnums.Seek.LASTEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41e56-131">AdoEnums.Seek.AFTEREQ</span><span class="sxs-lookup"><span data-stu-id="41e56-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e56-132">AdoEnums.Seek.AFTER</span><span class="sxs-lookup"><span data-stu-id="41e56-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41e56-133">AdoEnums.Seek.BEFOREEQ</span><span class="sxs-lookup"><span data-stu-id="41e56-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41e56-134">AdoEnums.Seek.BEFORE</span><span class="sxs-lookup"><span data-stu-id="41e56-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

