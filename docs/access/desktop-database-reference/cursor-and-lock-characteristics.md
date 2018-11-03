---
title: カーソルとロックの特徴
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2b3d518ccd82ae2dbc3f280954848d58d8e617cd
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944992"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="e1e12-102">カーソルとロックの特徴</span><span class="sxs-lookup"><span data-stu-id="e1e12-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="e1e12-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e1e12-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1e12-104">カーソルの特性はプロバイダーの機能によって異なりますが、一般には、カーソルとロックの種類別に、次のような長所と短所があります。</span><span class="sxs-lookup"><span data-stu-id="e1e12-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1e12-105">カーソルまたはロックの種類</span><span class="sxs-lookup"><span data-stu-id="e1e12-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="e1e12-106">長所</span><span class="sxs-lookup"><span data-stu-id="e1e12-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="e1e12-107">デメリット</span><span class="sxs-lookup"><span data-stu-id="e1e12-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1e12-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-109">必要なリソースが少ない</span><span class="sxs-lookup"><span data-stu-id="e1e12-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-110">後方にスクロールできない</span><span class="sxs-lookup"><span data-stu-id="e1e12-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="e1e12-111">データの同時操作ができない</span><span class="sxs-lookup"><span data-stu-id="e1e12-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1e12-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-113">スクロールができる</span><span class="sxs-lookup"><span data-stu-id="e1e12-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-114">データの同時操作ができない</span><span class="sxs-lookup"><span data-stu-id="e1e12-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1e12-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-116">データの同時操作が部分的にできる</span><span class="sxs-lookup"><span data-stu-id="e1e12-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="e1e12-117">スクロールができる</span><span class="sxs-lookup"><span data-stu-id="e1e12-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-118">必要なリソースが比較的多い</span><span class="sxs-lookup"><span data-stu-id="e1e12-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="e1e12-119">ネットワークに接続されていない場合は使用できない</span><span class="sxs-lookup"><span data-stu-id="e1e12-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1e12-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-121">データの高度な同時操作ができる</span><span class="sxs-lookup"><span data-stu-id="e1e12-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="e1e12-122">スクロールができる</span><span class="sxs-lookup"><span data-stu-id="e1e12-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-123">必要なリソースが最も多い</span><span class="sxs-lookup"><span data-stu-id="e1e12-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="e1e12-124">ネットワークに接続されていない場合は使用できない</span><span class="sxs-lookup"><span data-stu-id="e1e12-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1e12-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-126">必要なリソースが少ない</span><span class="sxs-lookup"><span data-stu-id="e1e12-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="e1e12-127">拡張性が高い</span><span class="sxs-lookup"><span data-stu-id="e1e12-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-128">カーソルを通じてデータを更新できない</span><span class="sxs-lookup"><span data-stu-id="e1e12-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1e12-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-130">バッチ更新ができる</span><span class="sxs-lookup"><span data-stu-id="e1e12-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="e1e12-131">ネットワークに接続されていない場合も使用できる</span><span class="sxs-lookup"><span data-stu-id="e1e12-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="e1e12-132">他のユーザーがデータにアクセスできる</span><span class="sxs-lookup"><span data-stu-id="e1e12-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-133">データが複数のユーザーによって同時に変更される可能性がある</span><span class="sxs-lookup"><span data-stu-id="e1e12-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e1e12-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-135">ロックされているときは他のユーザーがデータを変更できない</span><span class="sxs-lookup"><span data-stu-id="e1e12-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-136">ロックされているときは他のユーザーがデータにアクセスできない</span><span class="sxs-lookup"><span data-stu-id="e1e12-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1e12-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="e1e12-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-138">他のユーザーがデータにアクセスできる</span><span class="sxs-lookup"><span data-stu-id="e1e12-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="e1e12-139">データが複数のユーザーによって同時に変更される可能性がある</span><span class="sxs-lookup"><span data-stu-id="e1e12-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

