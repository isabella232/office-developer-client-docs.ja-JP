---
title: CursorTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c394f8000f1d4ae7867d83974e0e186616145fb5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864028"
---
# <a name="cursortypeenum"></a><span data-ttu-id="55617-102">CursorTypeEnum</span><span class="sxs-lookup"><span data-stu-id="55617-102">CursorTypeEnum</span></span>

<span data-ttu-id="55617-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="55617-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="55617-104">[Recordset](recordset-object-ado.md) オブジェクトが使用するカーソルの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="55617-104">Specifies the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55617-105">定数</span><span class="sxs-lookup"><span data-stu-id="55617-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="55617-106">値</span><span class="sxs-lookup"><span data-stu-id="55617-106">Value</span></span></p></th>
<th><p><span data-ttu-id="55617-107">説明</span><span class="sxs-lookup"><span data-stu-id="55617-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55617-108"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="55617-108"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="55617-109">2</span><span class="sxs-lookup"><span data-stu-id="55617-109">2</span></span></p></td>
<td><p><span data-ttu-id="55617-p101">動的カーソルを使用します。他のユーザーによる追加、変更、および削除が表示され、プロバイダーがブックマークをサポートしていない場合を除き、<strong>Recordset</strong> 内でのすべての種類の移動を許可します。</span><span class="sxs-lookup"><span data-stu-id="55617-p101">Uses a dynamic cursor. Additions, changes, and deletions by other users are visible, and all types of movement through the <strong>Recordset</strong> are allowed, except for bookmarks, if the provider doesn't support them.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55617-112"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="55617-112"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="55617-113">0</span><span class="sxs-lookup"><span data-stu-id="55617-113">0</span></span></p></td>
<td><p><span data-ttu-id="55617-p102">既定値。前方スクロール カーソルを使用します。レコードのスクロール方向が前方向に限定されていることを除き、静的カーソルと同じ働きをします。<strong>Recordset</strong> のスクロールが 1 回だけで十分な場合は、これによってパフォーマンスを向上できます。</span><span class="sxs-lookup"><span data-stu-id="55617-p102">Default. Uses a forward-only cursor. Identical to a static cursor, except that you can only scroll forward through records. This improves performance when you need to make only one pass through a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55617-118"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="55617-118"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="55617-119">1</span><span class="sxs-lookup"><span data-stu-id="55617-119">1</span></span></p></td>
<td><p><span data-ttu-id="55617-p103">キーセット カーソルを使います。自分の <strong>Recordset</strong> から他のユーザーが削除したレコードはアクセスできませんが、他のユーザーが追加したレコードは表示できない点を除いて動的カーソルと同じです。他のユーザーが変更したデータは表示できます。</span><span class="sxs-lookup"><span data-stu-id="55617-p103">Uses a keyset cursor. Like a dynamic cursor, except that you can't see records that other users add, although records that other users delete are inaccessible from your <strong>Recordset</strong>. Data changes by other users are still visible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55617-123"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="55617-123"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="55617-124">3</span><span class="sxs-lookup"><span data-stu-id="55617-124">3</span></span></p></td>
<td><p><span data-ttu-id="55617-p104">静的カーソルを使用します。データの検索やレポートの生成に使用できるの静的コピーです。他のユーザーによる追加、変更、または削除は表示されません。</span><span class="sxs-lookup"><span data-stu-id="55617-p104">Uses a static cursor. A static copy of a set of records that you can use to find data or generate reports. Additions, changes, or deletions by other users are not visible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55617-128"><strong>adOpenUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="55617-128"><strong>adOpenUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="55617-129">-1</span><span class="sxs-lookup"><span data-stu-id="55617-129">-1</span></span></p></td>
<td><p><span data-ttu-id="55617-130">カーソルの種類を指定しません。</span><span class="sxs-lookup"><span data-stu-id="55617-130">Does not specify the type of cursor.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="55617-131">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="55617-131">ADO/WFC equivalent</span></span>

<span data-ttu-id="55617-132">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="55617-132">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55617-133">定数</span><span class="sxs-lookup"><span data-stu-id="55617-133">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55617-134">AdoEnums.CursorType.DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="55617-134">AdoEnums.CursorType.DYNAMIC</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55617-135">AdoEnums.CursorType.FORWARDONLY</span><span class="sxs-lookup"><span data-stu-id="55617-135">AdoEnums.CursorType.FORWARDONLY</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55617-136">AdoEnums.CursorType.KEYSET</span><span class="sxs-lookup"><span data-stu-id="55617-136">AdoEnums.CursorType.KEYSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55617-137">AdoEnums.CursorType.STATIC</span><span class="sxs-lookup"><span data-stu-id="55617-137">AdoEnums.CursorType.STATIC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55617-138">AdoEnums.CursorType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="55617-138">AdoEnums.CursorType.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

