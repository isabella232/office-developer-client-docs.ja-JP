---
title: カーソル optionenum (Access デスクトップデータベースリファレンス)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295199"
---
# <a name="cursoroptionenum"></a><span data-ttu-id="862cd-102">CursorOptionEnum</span><span class="sxs-lookup"><span data-stu-id="862cd-102">CursorOptionEnum</span></span>

<span data-ttu-id="862cd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="862cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="862cd-104">[Supports](supports-method-ado.md) メソッドがテストする機能を表します。</span><span class="sxs-lookup"><span data-stu-id="862cd-104">Specifies what functionality the [Supports](supports-method-ado.md) method should test for.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="862cd-105">定数</span><span class="sxs-lookup"><span data-stu-id="862cd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="862cd-106">値</span><span class="sxs-lookup"><span data-stu-id="862cd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="862cd-107">説明</span><span class="sxs-lookup"><span data-stu-id="862cd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="862cd-108"><strong>adAddNew</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-108"><strong>adAddNew</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-109">0x1000400</span><span class="sxs-lookup"><span data-stu-id="862cd-109">0x1000400</span></span></p></td>
<td><p><span data-ttu-id="862cd-110">新しいレコードを追加する <a href="addnew-method-ado.md">AddNew</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-110">Supports the <a href="addnew-method-ado.md">AddNew</a> method to add new records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-111"><strong>adapproxposition</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-111"><strong>adApproxPosition</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-112">0x4000</span><span class="sxs-lookup"><span data-stu-id="862cd-112">0x4000</span></span></p></td>
<td><p><span data-ttu-id="862cd-113"><a href="absoluteposition-property-ado.md">AbsolutePosition</a> プロパティと <a href="absolutepage-property-ado.md">AbsolutePage</a> プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-113">Supports the <a href="absoluteposition-property-ado.md">AbsolutePosition</a> and <a href="absolutepage-property-ado.md">AbsolutePage</a> properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-114"><strong>adbookmark</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-114"><strong>adBookmark</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="862cd-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="862cd-116">特定のレコードへのアクセスを確保する <a href="bookmark-property-ado.md">Bookmark</a> プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-116">Supports the <a href="bookmark-property-ado.md">Bookmark</a> property to gain access to specific records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-117"><strong>addelete</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-117"><strong>adDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-118">0x1000800</span><span class="sxs-lookup"><span data-stu-id="862cd-118">0x1000800</span></span></p></td>
<td><p><span data-ttu-id="862cd-119">レコードを削除する <a href="delete-method-ado-recordset.md">Delete</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-119">Supports the <a href="delete-method-ado-recordset.md">Delete</a> method to delete records.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-120"><strong>adfind</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-120"><strong>adFind</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-121">0x80000</span><span class="sxs-lookup"><span data-stu-id="862cd-121">0x80000</span></span></p></td>
<td><p><span data-ttu-id="862cd-122"><a href="recordset-object-ado.md">Recordset</a> 内の行の位置を確認する <a href="find-method-ado.md">Find</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-122">Supports the <a href="find-method-ado.md">Find</a> method to locate a row in a <a href="recordset-object-ado.md">Recordset</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-123"><strong>adHoldRecords</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-123"><strong>adHoldRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-124">0x100</span><span class="sxs-lookup"><span data-stu-id="862cd-124">0x100</span></span></p></td>
<td><p><span data-ttu-id="862cd-125">保留中のすべての変更をコミットせずに、新たなレコードを格納するか、または次の格納位置を変更します。</span><span class="sxs-lookup"><span data-stu-id="862cd-125">Retrieves more records or changes the next position without committing all pending changes.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-126"><strong>adindex</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-126"><strong>adIndex</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-127">0x100000</span><span class="sxs-lookup"><span data-stu-id="862cd-127">0x100000</span></span></p></td>
<td><p><span data-ttu-id="862cd-128">インデックスに名前を付ける <a href="index-property-ado.md">Index</a> プロパティをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-128">Supports the <a href="index-property-ado.md">Index</a> property to name an index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-129"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-129"><strong>adMovePrevious</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-130">0x200</span><span class="sxs-lookup"><span data-stu-id="862cd-130">0x200</span></span></p></td>
<td><p><span data-ttu-id="862cd-131">ブックマークを使用せずに現在のレコードの位置を後方に移動する <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> メソッドと <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> メソッド、および <a href="move-method-ado.md">Move</a> メソッドと <a href="getrows-method-ado.md">GetRows</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-131">Supports the <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> and <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> methods, and <a href="move-method-ado.md">Move</a> or <a href="getrows-method-ado.md">GetRows</a> methods to move the current record position backward without requiring bookmarks.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-132"><strong>adnotify</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-132"><strong>adNotify</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-133">0x40000</span><span class="sxs-lookup"><span data-stu-id="862cd-133">0x40000</span></span></p></td>
<td><p><span data-ttu-id="862cd-134">基になるデータ プロバイダーが通知をサポートしていることを示します (これにより <strong>Recordset</strong> イベントのサポートの有無が決まります)。</span><span class="sxs-lookup"><span data-stu-id="862cd-134">Indicates that the underlying data provider supports notifications (which determines whether <strong>Recordset</strong> events are supported).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-135"><strong>adresync</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-135"><strong>adResync</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-136">0x20000</span><span class="sxs-lookup"><span data-stu-id="862cd-136">0x20000</span></span></p></td>
<td><p><span data-ttu-id="862cd-137">基になるデータベースのカーソルにある可視データを更新する <a href="resync-method-ado.md">Resync</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-137">Supports the <a href="resync-method-ado.md">Resync</a> method to update the cursor with the data that is visible in the underlying database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-138"><strong>adseek</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-138"><strong>adSeek</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-139">0x200000</span><span class="sxs-lookup"><span data-stu-id="862cd-139">0x200000</span></span></p></td>
<td><p><span data-ttu-id="862cd-140"><strong>Recordset</strong> 内の行を検索する <a href="seek-method-ado.md">Seek</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-140">Supports the <a href="seek-method-ado.md">Seek</a> method to locate a row in a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-141"><strong>adUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-141"><strong>adUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-142">0x1008000</span><span class="sxs-lookup"><span data-stu-id="862cd-142">0x1008000</span></span></p></td>
<td><p><span data-ttu-id="862cd-143">既存のデータを変更する <a href="update-method-ado.md">Update</a> メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-143">Supports the <a href="update-method-ado.md">Update</a> method to modify existing data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-144"><strong>adUpdateBatch</strong></span><span class="sxs-lookup"><span data-stu-id="862cd-144"><strong>adUpdateBatch</strong></span></span></p></td>
<td><p><span data-ttu-id="862cd-145">「その他」</span><span class="sxs-lookup"><span data-stu-id="862cd-145">0x10000</span></span></p></td>
<td><p><span data-ttu-id="862cd-146">複数の変更をグループとしてプロバイダーに送信するバッチ更新 (<a href="updatebatch-method-ado.md">UpdateBatch</a> メソッドと <a href="cancelbatch-method-ado.md">CancelBatch</a> メソッド) をサポートします。</span><span class="sxs-lookup"><span data-stu-id="862cd-146">Supports batch updating (<a href="updatebatch-method-ado.md">UpdateBatch</a> and <a href="cancelbatch-method-ado.md">CancelBatch</a> methods) to transmit groups of changes to the provider.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="862cd-147">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="862cd-147">ADO/WFC equivalent</span></span>

<span data-ttu-id="862cd-148">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="862cd-148">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="862cd-149">定数</span><span class="sxs-lookup"><span data-stu-id="862cd-149">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="862cd-150">AdoEnums オプション</span><span class="sxs-lookup"><span data-stu-id="862cd-150">AdoEnums.CursorOption.ADDNEW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-151">AdoEnums のオプション。 approxposition</span><span class="sxs-lookup"><span data-stu-id="862cd-151">AdoEnums.CursorOption.APPROXPOSITION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-152">AdoEnums オプション。 BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="862cd-152">AdoEnums.CursorOption.BOOKMARK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-153">AdoEnums を削除します。</span><span class="sxs-lookup"><span data-stu-id="862cd-153">AdoEnums.CursorOption.DELETE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-154">AdoEnums オプション。検索</span><span class="sxs-lookup"><span data-stu-id="862cd-154">AdoEnums.CursorOption.FIND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-155">AdoEnums オプション。 HOLDRECORDS</span><span class="sxs-lookup"><span data-stu-id="862cd-155">AdoEnums.CursorOption.HOLDRECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-156">AdoEnums オプション。インデックス</span><span class="sxs-lookup"><span data-stu-id="862cd-156">AdoEnums.CursorOption.INDEX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-157">AdoEnums オプション。 MOVEPREVIOUS</span><span class="sxs-lookup"><span data-stu-id="862cd-157">AdoEnums.CursorOption.MOVEPREVIOUS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-158">AdoEnums オプションの通知</span><span class="sxs-lookup"><span data-stu-id="862cd-158">AdoEnums.CursorOption.NOTIFY</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-159">AdoEnums オプション。 RESYNC</span><span class="sxs-lookup"><span data-stu-id="862cd-159">AdoEnums.CursorOption.RESYNC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-160">AdoEnums オプション。シーク</span><span class="sxs-lookup"><span data-stu-id="862cd-160">AdoEnums.CursorOption.SEEK</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="862cd-161">AdoEnums オプション</span><span class="sxs-lookup"><span data-stu-id="862cd-161">AdoEnums.CursorOption.UPDATE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="862cd-162">AdoEnums。 UPDATEBATCH</span><span class="sxs-lookup"><span data-stu-id="862cd-162">AdoEnums.CursorOption.UPDATEBATCH</span></span></p></td>
</tr>
</tbody>
</table>

