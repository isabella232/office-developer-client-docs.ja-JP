---
title: カーソルとロックの属性
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50eadc486d00436a51b9f7341ef6e0ad2587a015
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476183"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="43296-102">カーソルとロックの属性</span><span class="sxs-lookup"><span data-stu-id="43296-102">Cursor and Lock Characteristics</span></span>


<span data-ttu-id="43296-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="43296-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="43296-104">カーソルの特性はプロバイダーの機能によって異なりますが、一般には、カーソルとロックの種類別に、次のような長所と短所があります。</span><span class="sxs-lookup"><span data-stu-id="43296-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43296-105">カーソルまたはロックの種類</span><span class="sxs-lookup"><span data-stu-id="43296-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="43296-106">長所</span><span class="sxs-lookup"><span data-stu-id="43296-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="43296-107">デメリット</span><span class="sxs-lookup"><span data-stu-id="43296-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43296-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="43296-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-109">必要なリソースが少ない</span><span class="sxs-lookup"><span data-stu-id="43296-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-110">後方にスクロールできない</span><span class="sxs-lookup"><span data-stu-id="43296-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="43296-111">データの同時操作ができない</span><span class="sxs-lookup"><span data-stu-id="43296-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43296-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="43296-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-113">スクロールができる</span><span class="sxs-lookup"><span data-stu-id="43296-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-114">データの同時操作ができない</span><span class="sxs-lookup"><span data-stu-id="43296-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43296-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="43296-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-116">データの同時操作が部分的にできる</span><span class="sxs-lookup"><span data-stu-id="43296-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="43296-117">スクロールができる</span><span class="sxs-lookup"><span data-stu-id="43296-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-118">必要なリソースが比較的多い</span><span class="sxs-lookup"><span data-stu-id="43296-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="43296-119">ネットワークに接続されていない場合は使用できない</span><span class="sxs-lookup"><span data-stu-id="43296-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43296-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="43296-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-121">データの高度な同時操作ができる</span><span class="sxs-lookup"><span data-stu-id="43296-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="43296-122">スクロールができる</span><span class="sxs-lookup"><span data-stu-id="43296-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-123">必要なリソースが最も多い</span><span class="sxs-lookup"><span data-stu-id="43296-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="43296-124">ネットワークに接続されていない場合は使用できない</span><span class="sxs-lookup"><span data-stu-id="43296-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43296-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="43296-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-126">必要なリソースが少ない</span><span class="sxs-lookup"><span data-stu-id="43296-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="43296-127">拡張性が高い</span><span class="sxs-lookup"><span data-stu-id="43296-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-128">カーソルを通じてデータを更新できない</span><span class="sxs-lookup"><span data-stu-id="43296-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43296-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="43296-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-130">バッチ更新ができる</span><span class="sxs-lookup"><span data-stu-id="43296-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="43296-131">ネットワークに接続されていない場合も使用できる</span><span class="sxs-lookup"><span data-stu-id="43296-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="43296-132">他のユーザーがデータにアクセスできる</span><span class="sxs-lookup"><span data-stu-id="43296-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-133">データが複数のユーザーによって同時に変更される可能性がある</span><span class="sxs-lookup"><span data-stu-id="43296-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43296-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="43296-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-135">ロックされているときは他のユーザーがデータを変更できない</span><span class="sxs-lookup"><span data-stu-id="43296-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-136">ロックされているときは他のユーザーがデータにアクセスできない</span><span class="sxs-lookup"><span data-stu-id="43296-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43296-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="43296-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-138">他のユーザーがデータにアクセスできる</span><span class="sxs-lookup"><span data-stu-id="43296-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="43296-139">データが複数のユーザーによって同時に変更される可能性がある</span><span class="sxs-lookup"><span data-stu-id="43296-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

