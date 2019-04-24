---
title: カーソルとロックの特性
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295290"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="8b08c-102">カーソルとロックの特性</span><span class="sxs-lookup"><span data-stu-id="8b08c-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="8b08c-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b08c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b08c-104">カーソルの特性はプロバイダーの機能によって異なりますが、一般には、カーソルとロックの種類別に、次のような長所と短所があります。</span><span class="sxs-lookup"><span data-stu-id="8b08c-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b08c-105">カーソルまたはロックの種類</span><span class="sxs-lookup"><span data-stu-id="8b08c-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="8b08c-106">メリット</span><span class="sxs-lookup"><span data-stu-id="8b08c-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="8b08c-107">デメリット</span><span class="sxs-lookup"><span data-stu-id="8b08c-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b08c-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-109">必要なリソースが少ない</span><span class="sxs-lookup"><span data-stu-id="8b08c-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-110">後方にスクロールできない</span><span class="sxs-lookup"><span data-stu-id="8b08c-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="8b08c-111">データの同時操作ができない</span><span class="sxs-lookup"><span data-stu-id="8b08c-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b08c-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-113">ネ</span><span class="sxs-lookup"><span data-stu-id="8b08c-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-114">データの同時操作ができない</span><span class="sxs-lookup"><span data-stu-id="8b08c-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b08c-115"><strong>adopenkeyset</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-116">データの同時操作が部分的にできる</span><span class="sxs-lookup"><span data-stu-id="8b08c-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="8b08c-117">ネ</span><span class="sxs-lookup"><span data-stu-id="8b08c-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-118">必要なリソースが比較的多い</span><span class="sxs-lookup"><span data-stu-id="8b08c-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="8b08c-119">ネットワークに接続されていない場合は使用できない</span><span class="sxs-lookup"><span data-stu-id="8b08c-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b08c-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-121">データの高度な同時操作ができる</span><span class="sxs-lookup"><span data-stu-id="8b08c-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="8b08c-122">ネ</span><span class="sxs-lookup"><span data-stu-id="8b08c-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-123">必要なリソースが最も多い</span><span class="sxs-lookup"><span data-stu-id="8b08c-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="8b08c-124">ネットワークに接続されていない場合は使用できない</span><span class="sxs-lookup"><span data-stu-id="8b08c-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b08c-125"><strong>adlockreadonly です</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-126">必要なリソースが少ない</span><span class="sxs-lookup"><span data-stu-id="8b08c-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="8b08c-127">拡張性が高い</span><span class="sxs-lookup"><span data-stu-id="8b08c-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-128">カーソルを通じてデータを更新できない</span><span class="sxs-lookup"><span data-stu-id="8b08c-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b08c-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-130">バッチ更新ができる</span><span class="sxs-lookup"><span data-stu-id="8b08c-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="8b08c-131">ネットワークに接続されていない場合も使用できる</span><span class="sxs-lookup"><span data-stu-id="8b08c-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="8b08c-132">他のユーザーがデータにアクセスできる</span><span class="sxs-lookup"><span data-stu-id="8b08c-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-133">データが複数のユーザーによって同時に変更される可能性がある</span><span class="sxs-lookup"><span data-stu-id="8b08c-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b08c-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-135">ロックされているときは他のユーザーがデータを変更できない</span><span class="sxs-lookup"><span data-stu-id="8b08c-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-136">ロックされているときは他のユーザーがデータにアクセスできない</span><span class="sxs-lookup"><span data-stu-id="8b08c-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b08c-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="8b08c-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-138">他のユーザーがデータにアクセスできる</span><span class="sxs-lookup"><span data-stu-id="8b08c-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b08c-139">データが複数のユーザーによって同時に変更される可能性がある</span><span class="sxs-lookup"><span data-stu-id="8b08c-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

