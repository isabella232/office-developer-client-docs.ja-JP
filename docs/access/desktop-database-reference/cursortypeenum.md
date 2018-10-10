---
title: CursorTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c254c41bb066887e659c86a29ec4a91ca0de9cdd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479071"
---
# <a name="cursortypeenum"></a><span data-ttu-id="866b1-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="866b1-102">CursorTypeEnum</span></span>


<span data-ttu-id="866b1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="866b1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="866b1-104">[Recordset](recordset-object-ado.md) オブジェクトが使用するカーソルの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="866b1-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="866b1-105">定数</span><span class="sxs-lookup"><span data-stu-id="866b1-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="866b1-106">値</span><span class="sxs-lookup"><span data-stu-id="866b1-106">Value</span></span></p></th>
<th><p><span data-ttu-id="866b1-107">説明</span><span class="sxs-lookup"><span data-stu-id="866b1-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="866b1-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="866b1-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="866b1-109">2</span><span class="sxs-lookup"><span data-stu-id="866b1-109">2</span></span></p></td>
<td><p><span data-ttu-id="866b1-p101">動的カーソルを使用します。他のユーザーによる追加、変更、および削除が表示され、プロバイダーがブックマークをサポートしていない場合を除き、<strong>Recordset</strong> 内でのすべての種類の移動を許可します。</span><span class="sxs-lookup"><span data-stu-id="866b1-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="866b1-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="866b1-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="866b1-113">0</span><span class="sxs-lookup"><span data-stu-id="866b1-113">0</span></span></p></td>
<td><p><span data-ttu-id="866b1-p102">既定値。前方スクロール カーソルを使用します。レコードのスクロール方向が前方向に限定されていることを除き、静的カーソルと同じ働きをします。<strong>Recordset</strong> のスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="866b1-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="866b1-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="866b1-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="866b1-119">1</span><span class="sxs-lookup"><span data-stu-id="866b1-119">1</span></span></p></td>
<td><p><span data-ttu-id="866b1-p103">キーセット カーソルを使います。自分の <strong>Recordset</strong> から他のユーザーが削除したレコードはアクセスできませんが、他のユーザーが追加したレコードは表示できない点を除いて動的カーソルと同じです。他のユーザーが変更したデータは表示できます。</span><span class="sxs-lookup"><span data-stu-id="866b1-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="866b1-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="866b1-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="866b1-124">3</span><span class="sxs-lookup"><span data-stu-id="866b1-124">3</span></span></p></td>
<td><p><span data-ttu-id="866b1-p104">静的カーソルを使用します。データの検索やレポートの生成に使用できるの静的コピーです。他のユーザーによる追加、変更、または削除は表示されません。</span><span class="sxs-lookup"><span data-stu-id="866b1-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="866b1-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="866b1-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="866b1-129">-1</span><span class="sxs-lookup"><span data-stu-id="866b1-129">-1</span></span></p></td>
<td><p><span data-ttu-id="866b1-130">カーソルの種類を指定しません。</span><span class="sxs-lookup"><span data-stu-id="866b1-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="866b1-131">**ADO/WFC 等価**</span><span class="sxs-lookup"><span data-stu-id="866b1-131">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="866b1-132">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="866b1-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="866b1-133">定数</span><span class="sxs-lookup"><span data-stu-id="866b1-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="866b1-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="866b1-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="866b1-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="866b1-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="866b1-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="866b1-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="866b1-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="866b1-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="866b1-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="866b1-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

