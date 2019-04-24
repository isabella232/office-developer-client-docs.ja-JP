---
title: FieldAttributeEnum (Access デスクトップデータベースリファレンス)
TOCTitle: FieldAttributeEnum
ms:assetid: 2d3a541e-a437-6108-ab0e-90c7884b3df7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249071(v=office.15)
ms:contentKeyID: 48543967
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 079c79af3d15a6a5864a7db7f8334393258cfd42
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292602"
---
# <a name="fieldattributeenum"></a><span data-ttu-id="aac67-102">FieldAttributeEnum</span><span class="sxs-lookup"><span data-stu-id="aac67-102">FieldAttributeEnum</span></span>

<span data-ttu-id="aac67-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="aac67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aac67-104">[Field](field-object-ado.md) オブジェクトの 1 つ以上の属性を表します。</span><span class="sxs-lookup"><span data-stu-id="aac67-104">Specifies one or more attributes of a [Field](field-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aac67-105">定数</span><span class="sxs-lookup"><span data-stu-id="aac67-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="aac67-106">値</span><span class="sxs-lookup"><span data-stu-id="aac67-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aac67-107">説明</span><span class="sxs-lookup"><span data-stu-id="aac67-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aac67-108"><strong>adfldcachedeferred</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-108"><strong>adFldCacheDeferred</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-109">0x1000</span><span class="sxs-lookup"><span data-stu-id="aac67-109">0x1000</span></span></p></td>
<td><p><span data-ttu-id="aac67-110">プロバイダーでフィールド値がキャッシュされ、その後の読み取りはキャッシュから行われることを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-110">Indicates that the provider caches field values and that subsequent reads are done from the cache.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-111"><strong>adfldfixed</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-111"><strong>adFldFixed</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-112">0x10</span><span class="sxs-lookup"><span data-stu-id="aac67-112">0x10</span></span></p></td>
<td><p><span data-ttu-id="aac67-113">フィールドが固定長データを含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-113">Indicates that the field contains fixed-length data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-114"><strong>adfldischapter</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-114"><strong>adFldIsChapter</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-115">0x2000</span><span class="sxs-lookup"><span data-stu-id="aac67-115">0x2000</span></span></p></td>
<td><p><span data-ttu-id="aac67-p101">フィールドがチャプター値を含み、この親フィールドに関連付けられた特定の子レコードセットを指定していることを示します。通常、チャプター フィールドはデータ シェイプやフィルター用に使います。</span><span class="sxs-lookup"><span data-stu-id="aac67-p101">Indicates that the field contains a chapter value, which specifies a specific child recordset related to this parent field. Typically chapter fields are used with data shaping or filters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-118"><strong>adfldiscollection</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-118"><strong>adFldIsCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-119">0x40000</span><span class="sxs-lookup"><span data-stu-id="aac67-119">0x40000</span></span></p></td>
<td><p><span data-ttu-id="aac67-120">レコードが示すリソースが、テキスト ファイルなどの単純なリソースではなく、フォルダーなどのように他のリソースのコレクションであることを、フィールドが表していることを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-120">Indicates that the field specifies that the resource represented by the record is a collection of other resources, such as a folder, rather than a simple resource, such as a text file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-121"><strong>adfldisdefaultstream</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-121"><strong>adFldIsDefaultStream</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-122">0x20000</span><span class="sxs-lookup"><span data-stu-id="aac67-122">0x20000</span></span></p></td>
<td><p><span data-ttu-id="aac67-123">フィールドが、レコードが示すリソースの既定ストリームを含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-123">Indicates that the field contains the default stream for the resource represented by the record.</span></span> <span data-ttu-id="aac67-124">たとえば、既定のストリームは、web サイトのルートフォルダーの HTML コンテンツにすることができます。これは、ルート URL が指定されたときに自動的に提供されます。</span><span class="sxs-lookup"><span data-stu-id="aac67-124">For example, the default stream can be the HTML content of a root folder on a website, which is automatically served when the root URL is specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-125"><strong>adfldisnullable</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-125"><strong>adFldIsNullable</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-126">0x20</span><span class="sxs-lookup"><span data-stu-id="aac67-126">0x20</span></span></p></td>
<td><p><span data-ttu-id="aac67-127">フィールドに null 値を指定できることを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-127">Indicates that the field accepts null values.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-128"><strong>adfldisrowurl</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-128"><strong>adFldIsRowURL</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-129">「その他」</span><span class="sxs-lookup"><span data-stu-id="aac67-129">0x10000</span></span></p></td>
<td><p><span data-ttu-id="aac67-130">フィールドが、レコードが示すデータ ストアのリソースを指定する URL を含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-130">Indicates that the field contains the URL that names the resource from the data store represented by the record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-131"><strong>adFldLong</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-131"><strong>adFldLong</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-132">0x80</span><span class="sxs-lookup"><span data-stu-id="aac67-132">0x80</span></span></p></td>
<td><p><span data-ttu-id="aac67-p103">フィールドがロング バイナリ型のフィールドであることを示します。また、<a href="appendchunk-method-ado.md">AppendChunk</a> メソッドと <a href="getchunk-method-ado.md">GetChunk</a> メソッドを使用できることを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-p103">Indicates that the field is a long binary field. Also indicates that you can use the <a href="appendchunk-method-ado.md">AppendChunk</a> and <a href="getchunk-method-ado.md">GetChunk</a> methods.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-135"><strong>adFldMayBeNull</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-135"><strong>adFldMayBeNull</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-136">0x40</span><span class="sxs-lookup"><span data-stu-id="aac67-136">0x40</span></span></p></td>
<td><p><span data-ttu-id="aac67-137">フィールドからの null 値の読み取りが可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-137">Indicates that you can read null values from the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-138"><strong>adfld/defer</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-138"><strong>adFldMayDefer</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-139">0x2</span><span class="sxs-lookup"><span data-stu-id="aac67-139">0x2</span></span></p></td>
<td><p><span data-ttu-id="aac67-140">フィールドが遅延フィールドであることを示します。フィールド値は、レコード全体のデータ ソースから取得されず、明示的にアクセスした場合のみ取得されます。</span><span class="sxs-lookup"><span data-stu-id="aac67-140">Indicates that the field is deferred — that is, the field values are not retrieved from the data source with the whole record, but only when you explicitly access them.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-141"><strong>adFldNegativeScale</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-141"><strong>adFldNegativeScale</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-142">0x4000</span><span class="sxs-lookup"><span data-stu-id="aac67-142">0x4000</span></span></p></td>
<td><p><span data-ttu-id="aac67-p104">負のスケール値をサポートする列の数値を、フィールドが表していることを示します。スケールは、<a href="numericscale-property-ado.md">NumericScale</a> プロパティで指定します。</span><span class="sxs-lookup"><span data-stu-id="aac67-p104">Indicates that the field represents a numeric value from a column that supports negative scale values. The scale is specified by the <a href="numericscale-property-ado.md">NumericScale</a> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-145"><strong>adflん wid</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-145"><strong>adFldRowID</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-146">0x100</span><span class="sxs-lookup"><span data-stu-id="aac67-146">0x100</span></span></p></td>
<td><p><span data-ttu-id="aac67-147">フィールドが書き込み禁止の永続化された行識別子を含み、行を識別するもの (レコード番号、一意識別子など) 以外に有効な値は持たないことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-147">Indicates that the field contains a persistent row identifier that cannot be written to and has no meaningful value except to identify the row (such as a record number, unique identifier, and so forth).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-148"><strong>adFldRowVersion</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-148"><strong>adFldRowVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-149">0x200</span><span class="sxs-lookup"><span data-stu-id="aac67-149">0x200</span></span></p></td>
<td><p><span data-ttu-id="aac67-150">フィールドが更新を記録するための時刻または日付スタンプを含むことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-150">Indicates that the field contains some kind of time or date stamp used to track updates.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-151"><strong>adFldUnknownUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-151"><strong>adFldUnknownUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-152">0x8</span><span class="sxs-lookup"><span data-stu-id="aac67-152">0x8</span></span></p></td>
<td><p><span data-ttu-id="aac67-153">フィールドへの書き込みが可能かどうかをプロバイダーが確認できないことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-153">Indicates that the provider cannot determine if you can write to the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-154"><strong>adfldunspecified</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-154"><strong>adFldUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-155">-1</span><span class="sxs-lookup"><span data-stu-id="aac67-155">-1</span></span><br />
<span data-ttu-id="aac67-156">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="aac67-156">0xFFFFFFFF</span></span></p></td>
<td><p><span data-ttu-id="aac67-157">プロバイダーがフィールド属性を指定しないことを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-157">Indicates that the provider does not specify the field attributes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-158"><strong>adFldUpdatable</strong></span><span class="sxs-lookup"><span data-stu-id="aac67-158"><strong>adFldUpdatable</strong></span></span></p></td>
<td><p><span data-ttu-id="aac67-159">0x4</span><span class="sxs-lookup"><span data-stu-id="aac67-159">0x4</span></span></p></td>
<td><p><span data-ttu-id="aac67-160">フィールドへの書き込みが可能であることを示します。</span><span class="sxs-lookup"><span data-stu-id="aac67-160">Indicates that you can write to the field.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="aac67-161">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="aac67-161">ADO/WFC equivalent</span></span>

<span data-ttu-id="aac67-162">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="aac67-162">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aac67-163">定数</span><span class="sxs-lookup"><span data-stu-id="aac67-163">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aac67-164">FieldAttribute の遅延 AdoEnums</span><span class="sxs-lookup"><span data-stu-id="aac67-164">AdoEnums.FieldAttribute.CACHEDEFERRED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-165">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="aac67-165">AdoEnums.FieldAttribute.FIXED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-166">AdoEnums FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-166">AdoEnums.FieldAttribute.ISNULLABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-167">AdoEnums FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-167">AdoEnums.FieldAttribute.LONG</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-168">AdoEnums FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-168">AdoEnums.FieldAttribute.MAYBENULL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-169">AdoEnums。 FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-169">AdoEnums.FieldAttribute.MAYDEFER</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-170">AdoEnums FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-170">AdoEnums.FieldAttribute.NEGATIVESCALE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-171">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="aac67-171">AdoEnums.FieldAttribute.ROWID</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-172">AdoEnums FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-172">AdoEnums.FieldAttribute.ROWVERSION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-173">AdoEnums FieldAttribute</span><span class="sxs-lookup"><span data-stu-id="aac67-173">AdoEnums.FieldAttribute.UNKNOWNUPDATABLE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac67-174">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="aac67-174">AdoEnums.FieldAttribute.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac67-175">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="aac67-175">AdoEnums.FieldAttribute.UPDATABLE</span></span></p></td>
</tr>
</tbody>
</table>

