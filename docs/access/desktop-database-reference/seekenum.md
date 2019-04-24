---
title: seekenum (Access デスクトップデータベースリファレンス)
TOCTitle: SeekEnum
ms:assetid: a0574809-db2d-8759-18cc-fb1cf776e8fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249737(v=office.15)
ms:contentKeyID: 48546706
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2f8334cbfc8e0f6a362a36e03984739d1d52b6f6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314659"
---
# <a name="seekenum"></a><span data-ttu-id="a8aa2-102">SeekEnum</span><span class="sxs-lookup"><span data-stu-id="a8aa2-102">SeekEnum</span></span>

<span data-ttu-id="a8aa2-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8aa2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8aa2-104">実行する [Seek](seek-method-ado.md) の種類を表します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-104">Specifies the type of [Seek](seek-method-ado.md) to execute.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8aa2-105">定数</span><span class="sxs-lookup"><span data-stu-id="a8aa2-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="a8aa2-106">値</span><span class="sxs-lookup"><span data-stu-id="a8aa2-106">Value</span></span></p></th>
<th><p><span data-ttu-id="a8aa2-107">説明</span><span class="sxs-lookup"><span data-stu-id="a8aa2-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8aa2-108">adseekの手順 q</span><span class="sxs-lookup"><span data-stu-id="a8aa2-108">adSeekFirstEQ</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-109">1-d</span><span class="sxs-lookup"><span data-stu-id="a8aa2-109">1</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-110"><em>KeyValues</em> と一致する最初のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-110">Seeks the first key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8aa2-111">adseeklasteq</span><span class="sxs-lookup"><span data-stu-id="a8aa2-111">adSeekLastEQ</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-112">pbm-2</span><span class="sxs-lookup"><span data-stu-id="a8aa2-112">2</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-113"><em>KeyValues</em> と一致する最後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-113">Seeks the last key equal to <em>KeyValues</em>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8aa2-114">adseekaftereq</span><span class="sxs-lookup"><span data-stu-id="a8aa2-114">adSeekAfterEQ</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-115">2/4</span><span class="sxs-lookup"><span data-stu-id="a8aa2-115">4</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-116"><em>KeyValues</em> と一致するキー、またはその直後のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-116">Seeks either a key equal to <em>KeyValues</em> or just after where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8aa2-117">adseekafter</span><span class="sxs-lookup"><span data-stu-id="a8aa2-117">adSeekAfter</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-118">~</span><span class="sxs-lookup"><span data-stu-id="a8aa2-118">8</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-119"><em>KeyValues</em> と一致するキーの直後のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-119">Seeks a key just after where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8aa2-120">adseekbeforeeq</span><span class="sxs-lookup"><span data-stu-id="a8aa2-120">adSeekBeforeEQ</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-121">16</span><span class="sxs-lookup"><span data-stu-id="a8aa2-121">16</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-122"><em>KeyValues</em> と一致するキー、またはその直前のキーのいずれかを検索します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-122">Seeks either a key equal to <em>KeyValues</em> or just before where that match would have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8aa2-123">adseekbefore</span><span class="sxs-lookup"><span data-stu-id="a8aa2-123">adSeekBefore</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-124">32</span><span class="sxs-lookup"><span data-stu-id="a8aa2-124">32</span></span></p></td>
<td><p><span data-ttu-id="a8aa2-125"><em>KeyValues</em> と一致するキーの直前のキーを検索します。</span><span class="sxs-lookup"><span data-stu-id="a8aa2-125">Seeks a key just before where a match with <em>KeyValues</em> would have occurred.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="a8aa2-126">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="a8aa2-126">ADO/WFC equivalent</span></span>

<span data-ttu-id="a8aa2-127">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="a8aa2-127">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a8aa2-128">定数</span><span class="sxs-lookup"><span data-stu-id="a8aa2-128">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8aa2-129">AdoEnums (問)</span><span class="sxs-lookup"><span data-stu-id="a8aa2-129">AdoEnums.Seek.FIRSTEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8aa2-130">AdoEnums の自動応答</span><span class="sxs-lookup"><span data-stu-id="a8aa2-130">AdoEnums.Seek.LASTEQ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8aa2-131">AdoEnums eq</span><span class="sxs-lookup"><span data-stu-id="a8aa2-131">AdoEnums.Seek.AFTEREQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8aa2-132">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="a8aa2-132">AdoEnums.Seek.AFTER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8aa2-133">AdoEnums eq</span><span class="sxs-lookup"><span data-stu-id="a8aa2-133">AdoEnums.Seek.BEFOREEQ</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8aa2-134">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="a8aa2-134">AdoEnums.Seek.BEFORE</span></span></p></td>
</tr>
</tbody>
</table>

