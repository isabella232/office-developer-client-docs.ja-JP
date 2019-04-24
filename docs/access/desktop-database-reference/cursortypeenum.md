---
title: カーソル typeenum (Access デスクトップデータベースリファレンス)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295164"
---
# <a name="cursortypeenum"></a><span data-ttu-id="2220d-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="2220d-102">CursorTypeEnum</span></span>

<span data-ttu-id="2220d-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="2220d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2220d-104">[Recordset](recordset-object-ado.md) オブジェクトが使用するカーソルの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="2220d-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2220d-105">定数</span><span class="sxs-lookup"><span data-stu-id="2220d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2220d-106">値</span><span class="sxs-lookup"><span data-stu-id="2220d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2220d-107">説明</span><span class="sxs-lookup"><span data-stu-id="2220d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2220d-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="2220d-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="2220d-109">pbm-2</span><span class="sxs-lookup"><span data-stu-id="2220d-109">2</span></span></p></td>
<td><p><span data-ttu-id="2220d-p101">動的カーソルを使用します。他のユーザーによる追加、変更、および削除が表示され、プロバイダーがブックマークをサポートしていない場合を除き、<strong>Recordset</strong> 内でのすべての種類の移動を許可します。</span><span class="sxs-lookup"><span data-stu-id="2220d-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2220d-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="2220d-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="2220d-113">.0</span><span class="sxs-lookup"><span data-stu-id="2220d-113">0</span></span></p></td>
<td><p><span data-ttu-id="2220d-p102">既定値。前方スクロール カーソルを使用します。レコードのスクロール方向が前方向に限定されていることを除き、静的カーソルと同じ働きをします。<strong>Recordset</strong> のスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="2220d-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2220d-118"><strong>adopenkeyset</strong></span><span class="sxs-lookup"><span data-stu-id="2220d-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="2220d-119">1-d</span><span class="sxs-lookup"><span data-stu-id="2220d-119">1</span></span></p></td>
<td><p><span data-ttu-id="2220d-p103">キーセット カーソルを使います。自分の <strong>Recordset</strong> から他のユーザーが削除したレコードはアクセスできませんが、他のユーザーが追加したレコードは表示できない点を除いて動的カーソルと同じです。他のユーザーが変更したデータは表示できます。</span><span class="sxs-lookup"><span data-stu-id="2220d-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2220d-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="2220d-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="2220d-124">1/3</span><span class="sxs-lookup"><span data-stu-id="2220d-124">3</span></span></p></td>
<td><p><span data-ttu-id="2220d-p104">静的カーソルを使用します。データの検索やレポートの生成に使用できるの静的コピーです。他のユーザーによる追加、変更、または削除は表示されません。</span><span class="sxs-lookup"><span data-stu-id="2220d-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2220d-128"><strong>adopenunspecified</strong></span><span class="sxs-lookup"><span data-stu-id="2220d-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="2220d-129">-1</span><span class="sxs-lookup"><span data-stu-id="2220d-129">-1</span></span></p></td>
<td><p><span data-ttu-id="2220d-130">カーソルの種類を指定しません。</span><span class="sxs-lookup"><span data-stu-id="2220d-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2220d-131">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="2220d-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="2220d-132">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="2220d-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2220d-133">定数</span><span class="sxs-lookup"><span data-stu-id="2220d-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2220d-134">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="2220d-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2220d-135">AdoEnums CursorType</span><span class="sxs-lookup"><span data-stu-id="2220d-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2220d-136">AdoEnums。 CursorType</span><span class="sxs-lookup"><span data-stu-id="2220d-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2220d-137">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="2220d-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2220d-138">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="2220d-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

