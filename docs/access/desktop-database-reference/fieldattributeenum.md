---
title: FieldAttributeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706878"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="e56a8-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="e56a8-102">FieldAttributeEnum</span></span>

<span data-ttu-id="e56a8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="e56a8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e56a8-104">[Field](field-object-ado.md) オブジェクトの 1 つ以上の属性を表します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e56a8-105">定数</span><span class="sxs-lookup"><span data-stu-id="e56a8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e56a8-106">値</span><span class="sxs-lookup"><span data-stu-id="e56a8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e56a8-107">説明</span><span class="sxs-lookup"><span data-stu-id="e56a8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-108"><strong>adFldCacheDeferred</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="e56a8-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="e56a8-110">プロバイダーでフィールド値がキャッシュされ、その後の読み取りはキャッシュから行われることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-111"><strong>adFldFixed</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-112">0x10</span><span class="sxs-lookup"><span data-stu-id="e56a8-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="e56a8-113">フィールドが固定長データを含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-114"><strong>adFldIsChapter</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="e56a8-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="e56a8-p101">フィールドがチャプター値を含み、この親フィールドに関連付けられた特定の子レコードセットを指定していることを示します。通常、チャプター フィールドはデータ シェイプやフィルター用に使います。</span><span class="sxs-lookup"><span data-stu-id="e56a8-p101">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field. Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-118"><strong>adFldIsCollection</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="e56a8-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="e56a8-120">レコードが示すリソースが、テキスト ファイルなどの単純なリソースではなく、フォルダーなどのように他のリソースのコレクションであることを、フィールドが表していることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-121"><strong>adFldIsDefaultStream</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="e56a8-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="e56a8-123">フィールドにレコードが示すリソースの既定のストリームが含まれていることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="e56a8-124">たとえば、既定のストリームには、ルート URL を指定すると自動的に提供される web サイトのルート フォルダーの HTML コンテンツができます。</span><span class="sxs-lookup"><span data-stu-id="e56a8-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-125"><strong>adFldIsNullable</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-126">0x20</span><span class="sxs-lookup"><span data-stu-id="e56a8-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="e56a8-127">フィールドに null 値を指定できることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-128"><strong>adFldIsRowURL</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-129">0x10000</span><span class="sxs-lookup"><span data-stu-id="e56a8-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="e56a8-130">フィールドが、レコードが示すデータ ストアのリソースを指定する URL を含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-132">0x80</span><span class="sxs-lookup"><span data-stu-id="e56a8-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="e56a8-p103">フィールドがロング バイナリ型のフィールドであることを示します。また、<a href="appendchunk-method-ado.md">AppendChunk</a> メソッドと <a href="getchunk-method-ado.md">GetChunk</a> メソッドを使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-p103">Indicates that the field is a long binary field. Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-136">0x40</span><span class="sxs-lookup"><span data-stu-id="e56a8-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="e56a8-137">フィールドからの null 値の読み取りが可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-138"><strong>adFldMayDefer</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-139">0x2</span><span class="sxs-lookup"><span data-stu-id="e56a8-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="e56a8-140">フィールドが遅延フィールドであることを示します。フィールド値は、レコード全体のデータ ソースから取得されず、明示的にアクセスした場合のみ取得されます。</span><span class="sxs-lookup"><span data-stu-id="e56a8-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="e56a8-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="e56a8-p104">負のスケール値をサポートする列の数値を、フィールドが表していることを示します。スケールは、<a href="numericscale-property-ado.md">NumericScale</a> プロパティで指定します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-p104">Indicates that the field represents a numeric value from a column that supports negative scale values. The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-145"><strong>adFldRowID</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-146">0x100</span><span class="sxs-lookup"><span data-stu-id="e56a8-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="e56a8-147">フィールドが書き込み禁止の永続化された行識別子を含み、行を識別するもの (レコード番号、一意識別子など) 以外に有効な値は持たないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-149">0x200</span><span class="sxs-lookup"><span data-stu-id="e56a8-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="e56a8-150">フィールドが更新を記録するための時刻または日付スタンプを含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-152">0x8</span><span class="sxs-lookup"><span data-stu-id="e56a8-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="e56a8-153">フィールドへの書き込みが可能かどうかをプロバイダーが確認できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-154"><strong>adFldUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-155">-1</span><span class="sxs-lookup"><span data-stu-id="e56a8-155">-1</span></span><br />
<span data-ttu-id="e56a8-156">0 xffffffff</span><span class="sxs-lookup"><span data-stu-id="e56a8-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="e56a8-157">プロバイダーがフィールド属性を指定しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="e56a8-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="e56a8-159">0x4</span><span class="sxs-lookup"><span data-stu-id="e56a8-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="e56a8-160">フィールドへの書き込みが可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="e56a8-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e56a8-161">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="e56a8-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="e56a8-162">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="e56a8-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e56a8-163">定数</span><span class="sxs-lookup"><span data-stu-id="e56a8-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span><span class="sxs-lookup"><span data-stu-id="e56a8-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-165">AdoEnums.FieldAttribute.FIXED</span><span class="sxs-lookup"><span data-stu-id="e56a8-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-166">AdoEnums.FieldAttribute.ISNULLABLE</span><span class="sxs-lookup"><span data-stu-id="e56a8-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-167">AdoEnums.FieldAttribute.LONG</span><span class="sxs-lookup"><span data-stu-id="e56a8-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-168">AdoEnums.FieldAttribute.MAYBENULL</span><span class="sxs-lookup"><span data-stu-id="e56a8-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-169">AdoEnums.FieldAttribute.MAYDEFER</span><span class="sxs-lookup"><span data-stu-id="e56a8-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span><span class="sxs-lookup"><span data-stu-id="e56a8-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-171">AdoEnums.FieldAttribute.ROWID</span><span class="sxs-lookup"><span data-stu-id="e56a8-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-172">AdoEnums.FieldAttribute.ROWVERSION</span><span class="sxs-lookup"><span data-stu-id="e56a8-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span><span class="sxs-lookup"><span data-stu-id="e56a8-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e56a8-174">AdoEnums.FieldAttribute.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="e56a8-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e56a8-175">AdoEnums.FieldAttribute.UPDATABLE</span><span class="sxs-lookup"><span data-stu-id="e56a8-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

