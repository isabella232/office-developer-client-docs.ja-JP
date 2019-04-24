---
title: errorvalueenum (Access デスクトップデータベースリファレンス)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c2d4207f157d361f3b8aba2ff80f46d06b2f328e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293323"
---
# <a name="errorvalueenum"></a><span data-ttu-id="3568a-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="3568a-102">ErrorValueEnum</span></span>

<span data-ttu-id="3568a-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="3568a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3568a-104">ADO 実行時エラーの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="3568a-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="3568a-105">エラー番号には次の 3 種類の形式があります。</span><span class="sxs-lookup"><span data-stu-id="3568a-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="3568a-p101">正の 10 進値: 10 進数で表された完全エラー番号の下位 2 バイト。この数値は、Visual Basic の既定のエラー メッセージ ダイアログ ボックスに表示されます。たとえば、実行時エラー '3707' がその例です。</span><span class="sxs-lookup"><span data-stu-id="3568a-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="3568a-109">負の 10 進値: 完全エラー番号を 10 進数に変換したもの。</span><span class="sxs-lookup"><span data-stu-id="3568a-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="3568a-110">16 進値: 完全エラー番号の 16 進数表記。</span><span class="sxs-lookup"><span data-stu-id="3568a-110">Hexadecimal — The hexadecimal representation of the full error number.</span></span> <span data-ttu-id="3568a-111">Windows 機能コードは 4 桁目です。</span><span class="sxs-lookup"><span data-stu-id="3568a-111">The Windows facility code is in the fourth digit.</span></span> <span data-ttu-id="3568a-112">ADO エラー番号のファシリティコードは *、* です。例: 0x800***A***0e7b。</span><span class="sxs-lookup"><span data-stu-id="3568a-112">The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="3568a-113">OLE DB エラーが ADO アプリケーションに渡される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3568a-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="3568a-114">通常、これらは Windows ファシリティコード*4*で識別できます。</span><span class="sxs-lookup"><span data-stu-id="3568a-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="3568a-115">たとえば、0x800_**4**_....これらの番号の詳細については、「 *OLE DB プログラマリファレンス*」の「16章」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3568a-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3568a-116">定数</span><span class="sxs-lookup"><span data-stu-id="3568a-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="3568a-117">値</span><span class="sxs-lookup"><span data-stu-id="3568a-117">Value</span></span></p></th>
<th><p><span data-ttu-id="3568a-118">説明</span><span class="sxs-lookup"><span data-stu-id="3568a-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3568a-119"><strong>aderrboundtocommand</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-120">3707</span><span class="sxs-lookup"><span data-stu-id="3568a-120">3707</span></span><br />
<span data-ttu-id="3568a-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="3568a-121">-2146824581</span></span><br />
<span data-ttu-id="3568a-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="3568a-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="3568a-123"><strong>Command</strong> オブジェクトをソースに持つ <strong>Recordset</strong> オブジェクトの <strong>ActiveConnection</strong> プロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-125">3732</span><span class="sxs-lookup"><span data-stu-id="3568a-125">3732</span></span><br />
<span data-ttu-id="3568a-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="3568a-126">-2146824556</span></span><br />
<span data-ttu-id="3568a-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="3568a-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="3568a-128">サーバーは操作を完了できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-130">3748</span><span class="sxs-lookup"><span data-stu-id="3568a-130">3748</span></span><br />
<span data-ttu-id="3568a-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="3568a-131">-2146824540</span></span><br />
<span data-ttu-id="3568a-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="3568a-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="3568a-133">接続が拒否されました。</span><span class="sxs-lookup"><span data-stu-id="3568a-133">Connection was denied.</span></span> <span data-ttu-id="3568a-134">要求された新規接続の特性が現在使用中の特性と異なります。</span><span class="sxs-lookup"><span data-stu-id="3568a-134">New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-135"><strong>aderrcantchangeprovider</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-136">3220</span><span class="sxs-lookup"><span data-stu-id="3568a-136">3220</span></span><br />
<span data-ttu-id="3568a-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="3568a-137">-2146825068</span></span><br />
<span data-ttu-id="3568a-138">0x800a0c94</span><span class="sxs-lookup"><span data-stu-id="3568a-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="3568a-139">指定されたプロバイダーが既に使用されているものと異なります。</span><span class="sxs-lookup"><span data-stu-id="3568a-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-140"><strong>aderrcantconvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-141">3724</span><span class="sxs-lookup"><span data-stu-id="3568a-141">3724</span></span><br />
<span data-ttu-id="3568a-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="3568a-142">-2146824564</span></span><br />
<span data-ttu-id="3568a-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="3568a-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="3568a-144">符号の不一致またはデータ オーバーフロー以外の理由により、データ値を変換できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-144">Data value cannot be converted for reasons other than sign mismatch or data overflow.</span></span> <span data-ttu-id="3568a-145">たとえば、変換によりデータの一部が切り捨てられる場合などです。</span><span class="sxs-lookup"><span data-stu-id="3568a-145">For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-146"><strong>aderrcantcreate</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-147">3725</span><span class="sxs-lookup"><span data-stu-id="3568a-147">3725</span></span><br />
<span data-ttu-id="3568a-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="3568a-148">-2146824563</span></span><br />
<span data-ttu-id="3568a-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="3568a-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="3568a-150">フィールドのデータ型が不明であったか、プロバイダーが操作を実行するのに十分なリソースを持っていなかったため、データ値を設定または取得できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-151"><strong>aderrcatalognotset</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-152">3747</span><span class="sxs-lookup"><span data-stu-id="3568a-152">3747</span></span><br />
<span data-ttu-id="3568a-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="3568a-153">-2146824541</span></span><br />
<span data-ttu-id="3568a-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="3568a-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="3568a-155">操作には有効な <strong>ParentCatalog</strong> が必要です。</span><span class="sxs-lookup"><span data-stu-id="3568a-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-156"><strong>aderrcolumnnotonこの行</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-157">3726</span><span class="sxs-lookup"><span data-stu-id="3568a-157">3726</span></span><br />
<span data-ttu-id="3568a-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="3568a-158">-2146824562</span></span><br />
<span data-ttu-id="3568a-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="3568a-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="3568a-160">レコードにこのフィールドが存在しません。</span><span class="sxs-lookup"><span data-stu-id="3568a-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-162">3421</span><span class="sxs-lookup"><span data-stu-id="3568a-162">3421</span></span><br />
<span data-ttu-id="3568a-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="3568a-163">-2146824867</span></span><br />
<span data-ttu-id="3568a-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="3568a-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="3568a-165">現在の操作に対して、間違った型の値を使用しています。</span><span class="sxs-lookup"><span data-stu-id="3568a-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-166"><strong>aderrdataoverflow</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-167">3721</span><span class="sxs-lookup"><span data-stu-id="3568a-167">3721</span></span><br />
<span data-ttu-id="3568a-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="3568a-168">-2146824567</span></span><br />
<span data-ttu-id="3568a-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="3568a-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="3568a-170">データ値が大きすぎるために、フィールドのデータ型で表現できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-172">3738</span><span class="sxs-lookup"><span data-stu-id="3568a-172">3738</span></span><br />
<span data-ttu-id="3568a-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="3568a-173">-2146824550</span></span><br />
<span data-ttu-id="3568a-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="3568a-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="3568a-175">削除されるオブジェクトの URL は現在のレコードの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="3568a-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-177">3750</span><span class="sxs-lookup"><span data-stu-id="3568a-177">3750</span></span><br />
<span data-ttu-id="3568a-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="3568a-178">-2146824538</span></span><br />
<span data-ttu-id="3568a-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="3568a-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="3568a-180">プロバイダーが共有の制約をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3568a-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-181"><strong>aderrdenytypenotsupported がサポートされている</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-182">3751</span><span class="sxs-lookup"><span data-stu-id="3568a-182">3751</span></span><br />
<span data-ttu-id="3568a-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="3568a-183">-2146824537</span></span><br />
<span data-ttu-id="3568a-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="3568a-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="3568a-185">プロバイダーが、要求された種類の共有の制約をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="3568a-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-187">3251</span><span class="sxs-lookup"><span data-stu-id="3568a-187">3251</span></span><br />
<span data-ttu-id="3568a-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="3568a-188">-2146825037</span></span><br />
<span data-ttu-id="3568a-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="3568a-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="3568a-190">オブジェクトまたはプロバイダーは要求された操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-192">3749</span><span class="sxs-lookup"><span data-stu-id="3568a-192">3749</span></span><br />
<span data-ttu-id="3568a-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="3568a-193">-2146824539</span></span><br />
<span data-ttu-id="3568a-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="3568a-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="3568a-195">フィールドを更新できませんでした。</span><span class="sxs-lookup"><span data-stu-id="3568a-195">Fields update failed.</span></span> <span data-ttu-id="3568a-196">詳細については、各 Field オブジェクトの <strong>Status</strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="3568a-196">For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-198">3219</span><span class="sxs-lookup"><span data-stu-id="3568a-198">3219</span></span><br />
<span data-ttu-id="3568a-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="3568a-199">-2146825069</span></span><br />
<span data-ttu-id="3568a-200">0x800a0c93</span><span class="sxs-lookup"><span data-stu-id="3568a-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="3568a-201">このコンテキストで操作は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="3568a-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-203">3719</span><span class="sxs-lookup"><span data-stu-id="3568a-203">3719</span></span><br />
<span data-ttu-id="3568a-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="3568a-204">-2146824569</span></span><br />
<span data-ttu-id="3568a-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="3568a-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="3568a-206">データの値がフィールドの整合性制約に反しています。</span><span class="sxs-lookup"><span data-stu-id="3568a-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-207"><strong>aderrintransaction</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-208">3246</span><span class="sxs-lookup"><span data-stu-id="3568a-208">3246</span></span><br />
<span data-ttu-id="3568a-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="3568a-209">-2146825042</span></span><br />
<span data-ttu-id="3568a-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="3568a-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="3568a-211">トランザクションの実行中に <strong>Connection</strong> オブジェクトを明示的に閉じることができません。</span><span class="sxs-lookup"><span data-stu-id="3568a-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-213">3001</span><span class="sxs-lookup"><span data-stu-id="3568a-213">3001</span></span><br />
<span data-ttu-id="3568a-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="3568a-214">-2146825287</span></span><br />
<span data-ttu-id="3568a-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="3568a-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="3568a-216">間違った種類または許容範囲外の引数を使用しているか、使用している引数が競合しています。</span><span class="sxs-lookup"><span data-stu-id="3568a-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-217"><strong>aderrinvalidconnection</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-218">3709</span><span class="sxs-lookup"><span data-stu-id="3568a-218">3709</span></span><br />
<span data-ttu-id="3568a-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="3568a-219">-2146824579</span></span><br />
<span data-ttu-id="3568a-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="3568a-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="3568a-221">この操作を実行するために接続を使用できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-221">The connection cannot be used to perform this operation.</span></span> <span data-ttu-id="3568a-222">このコンテキストで閉じているかあるいは無効です。</span><span class="sxs-lookup"><span data-stu-id="3568a-222">It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-223"><strong>aderrinvalidparaminfo</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-224">3708</span><span class="sxs-lookup"><span data-stu-id="3568a-224">3708</span></span><br />
<span data-ttu-id="3568a-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="3568a-225">-2146824580</span></span><br />
<span data-ttu-id="3568a-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="3568a-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="3568a-227"><strong>Parameter</strong> オブジェクトが適切に定義されていません。</span><span class="sxs-lookup"><span data-stu-id="3568a-227"><strong>Parameter</strong> object is improperly defined.</span></span> <span data-ttu-id="3568a-228">矛盾した、または不完全な情報が指定されました。</span><span class="sxs-lookup"><span data-stu-id="3568a-228">Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-229"><strong>aderrinvalidtransaction</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-230">3714</span><span class="sxs-lookup"><span data-stu-id="3568a-230">3714</span></span><br />
<span data-ttu-id="3568a-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="3568a-231">-2146824574</span></span><br />
<span data-ttu-id="3568a-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="3568a-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="3568a-233">調整トランザクションが無効であるか、開始されていません。</span><span class="sxs-lookup"><span data-stu-id="3568a-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-234"><strong>aderrinvalidurl</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-235">3729</span><span class="sxs-lookup"><span data-stu-id="3568a-235">3729</span></span><br />
<span data-ttu-id="3568a-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="3568a-236">-2146824559</span></span><br />
<span data-ttu-id="3568a-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="3568a-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="3568a-238">URL に無効な文字が含まれています。</span><span class="sxs-lookup"><span data-stu-id="3568a-238">URL contains invalid characters.</span></span> <span data-ttu-id="3568a-239">URL が正しく入力されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="3568a-239">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-241">3265</span><span class="sxs-lookup"><span data-stu-id="3568a-241">3265</span></span><br />
<span data-ttu-id="3568a-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="3568a-242">-2146825023</span></span><br />
<span data-ttu-id="3568a-243">0x800A0CC1</span><span class="sxs-lookup"><span data-stu-id="3568a-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="3568a-244">要求された名前、または序数に対応する項目がコレクションで見つかりません。</span><span class="sxs-lookup"><span data-stu-id="3568a-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-246">3021</span><span class="sxs-lookup"><span data-stu-id="3568a-246">3021</span></span><br />
<span data-ttu-id="3568a-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="3568a-247">-2146825267</span></span><br />
<span data-ttu-id="3568a-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="3568a-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="3568a-249"><strong>BOF</strong> または <strong>EOF</strong> が True であるか、現在のレコードが削除されています。</span><span class="sxs-lookup"><span data-stu-id="3568a-249">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted.</span></span> <span data-ttu-id="3568a-250">要求された操作には現在のレコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="3568a-250">Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-251"><strong>aderrnotexecuting</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-252">3715</span><span class="sxs-lookup"><span data-stu-id="3568a-252">3715</span></span><br />
<span data-ttu-id="3568a-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="3568a-253">-2146824573</span></span><br />
<span data-ttu-id="3568a-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="3568a-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="3568a-255">実行していない間に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="3568a-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-256"><strong>aderrnotreentrant</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-257">3710</span><span class="sxs-lookup"><span data-stu-id="3568a-257">3710</span></span><br />
<span data-ttu-id="3568a-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="3568a-258">-2146824578</span></span><br />
<span data-ttu-id="3568a-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="3568a-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="3568a-260">イベント処理中に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="3568a-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-262">3704</span><span class="sxs-lookup"><span data-stu-id="3568a-262">3704</span></span><br />
<span data-ttu-id="3568a-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="3568a-263">-2146824584</span></span><br />
<span data-ttu-id="3568a-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="3568a-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="3568a-265">オブジェクトが閉じている場合は、操作は許可されません。</span><span class="sxs-lookup"><span data-stu-id="3568a-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-267">3367</span><span class="sxs-lookup"><span data-stu-id="3568a-267">3367</span></span><br />
<span data-ttu-id="3568a-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="3568a-268">-2146824921</span></span><br />
<span data-ttu-id="3568a-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="3568a-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="3568a-270">オブジェクトは既にコレクションに存在します。</span><span class="sxs-lookup"><span data-stu-id="3568a-270">Object is already in collection.</span></span> <span data-ttu-id="3568a-271">追加できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-271">Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-273">3420</span><span class="sxs-lookup"><span data-stu-id="3568a-273">3420</span></span><br />
<span data-ttu-id="3568a-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="3568a-274">-2146824868</span></span><br />
<span data-ttu-id="3568a-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="3568a-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="3568a-276">オブジェクトが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="3568a-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-278">3705</span><span class="sxs-lookup"><span data-stu-id="3568a-278">3705</span></span><br />
<span data-ttu-id="3568a-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="3568a-279">-2146824583</span></span><br />
<span data-ttu-id="3568a-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="3568a-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="3568a-281">オブジェクトが開いている場合は、操作は許可されません。</span><span class="sxs-lookup"><span data-stu-id="3568a-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-283">3002</span><span class="sxs-lookup"><span data-stu-id="3568a-283">3002</span></span><br />
<span data-ttu-id="3568a-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="3568a-284">-2146825286</span></span><br />
<span data-ttu-id="3568a-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="3568a-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="3568a-286">ファイルを開くことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="3568a-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-288">3712</span><span class="sxs-lookup"><span data-stu-id="3568a-288">3712</span></span><br />
<span data-ttu-id="3568a-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="3568a-289">-2146824576</span></span><br />
<span data-ttu-id="3568a-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="3568a-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="3568a-291">ユーザーにより操作が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="3568a-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-293">3734</span><span class="sxs-lookup"><span data-stu-id="3568a-293">3734</span></span><br />
<span data-ttu-id="3568a-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="3568a-294">-2146824554</span></span><br />
<span data-ttu-id="3568a-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="3568a-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="3568a-296">操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-296">Operation cannot be performed.</span></span> <span data-ttu-id="3568a-297">プロバイダーによって十分な記憶域が確保できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-297">Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-298"><strong>aderrpermissiondenied</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-299">3720</span><span class="sxs-lookup"><span data-stu-id="3568a-299">3720</span></span><br />
<span data-ttu-id="3568a-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="3568a-300">-2146824568</span></span><br />
<span data-ttu-id="3568a-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="3568a-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="3568a-302">権限不足のためフィールドの書き込みはできません。</span><span class="sxs-lookup"><span data-stu-id="3568a-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-303"><strong>aderrproviderfailed</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-304">3000</span><span class="sxs-lookup"><span data-stu-id="3568a-304">3000</span></span><br />
<span data-ttu-id="3568a-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="3568a-305">-2146825288</span></span><br />
<span data-ttu-id="3568a-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="3568a-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="3568a-307">プロバイダーが要求された操作を実行できませんでした。</span><span class="sxs-lookup"><span data-stu-id="3568a-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-309">3706</span><span class="sxs-lookup"><span data-stu-id="3568a-309">3706</span></span><br />
<span data-ttu-id="3568a-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="3568a-310">-2146824582</span></span><br />
<span data-ttu-id="3568a-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="3568a-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="3568a-312">プロバイダーが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="3568a-312">Provider cannot be found.</span></span> <span data-ttu-id="3568a-313">正しくインストールされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3568a-313">It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-314"><strong>aderrreadfile</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-315">3003</span><span class="sxs-lookup"><span data-stu-id="3568a-315">3003</span></span><br />
<span data-ttu-id="3568a-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="3568a-316">-2146825285</span></span><br />
<span data-ttu-id="3568a-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="3568a-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="3568a-318">ファイルを読み込むことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="3568a-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-319"><strong>aderrresourceexists</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-320">3731</span><span class="sxs-lookup"><span data-stu-id="3568a-320">3731</span></span><br />
<span data-ttu-id="3568a-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="3568a-321">-2146824557</span></span><br />
<span data-ttu-id="3568a-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="3568a-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="3568a-323">コピー操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-323">Copy operation cannot be performed.</span></span> <span data-ttu-id="3568a-324">宛先の URL で指定されたオブジェクトは既に存在します。</span><span class="sxs-lookup"><span data-stu-id="3568a-324">Object named by destination URL already exists.</span></span> <span data-ttu-id="3568a-325">オブジェクトを置き換えるためには <strong>adCopyOverwrite</strong> を指定してください。</span><span class="sxs-lookup"><span data-stu-id="3568a-325">Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-326"><strong>aderrresourcelocked</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-327">3730</span><span class="sxs-lookup"><span data-stu-id="3568a-327">3730</span></span><br />
<span data-ttu-id="3568a-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="3568a-328">-2146824558</span></span><br />
<span data-ttu-id="3568a-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="3568a-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="3568a-p115">指定された URL によって表されたオブジェクトは 1 つ以上の他のプロセスによってロックされています。プロセスが終了するまで待って、操作を再度実行してください。</span><span class="sxs-lookup"><span data-stu-id="3568a-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-333">3735</span><span class="sxs-lookup"><span data-stu-id="3568a-333">3735</span></span><br />
<span data-ttu-id="3568a-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="3568a-334">-2146824553</span></span><br />
<span data-ttu-id="3568a-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="3568a-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="3568a-336">ソースまたは宛先の URL が、現在のレコードの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="3568a-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-337"><strong>aderrschemaviolation</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-338">3722</span><span class="sxs-lookup"><span data-stu-id="3568a-338">3722</span></span><br />
<span data-ttu-id="3568a-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="3568a-339">-2146824566</span></span><br />
<span data-ttu-id="3568a-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="3568a-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="3568a-341">データ値がフィールドのデータ型と一致していないか、フィールドの制約に反しています。</span><span class="sxs-lookup"><span data-stu-id="3568a-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-342"><strong>aderrsignmismatch</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-343">3723</span><span class="sxs-lookup"><span data-stu-id="3568a-343">3723</span></span><br />
<span data-ttu-id="3568a-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="3568a-344">-2146824565</span></span><br />
<span data-ttu-id="3568a-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="3568a-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="3568a-346">データの値は符号付きですが、プロバイダーによって使用されるフィールド データ型は符号なしのため、変換に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="3568a-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-348">3713</span><span class="sxs-lookup"><span data-stu-id="3568a-348">3713</span></span><br />
<span data-ttu-id="3568a-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="3568a-349">-2146824575</span></span><br />
<span data-ttu-id="3568a-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="3568a-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="3568a-351">非同期操作の保留中に、操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="3568a-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-353">3711</span><span class="sxs-lookup"><span data-stu-id="3568a-353">3711</span></span><br />
<span data-ttu-id="3568a-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="3568a-354">-2146824577</span></span><br />
<span data-ttu-id="3568a-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="3568a-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="3568a-356">非同期実行中に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="3568a-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-357"><strong>aderrtreepermissiondenied</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-358">3728</span><span class="sxs-lookup"><span data-stu-id="3568a-358">3728</span></span><br />
<span data-ttu-id="3568a-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="3568a-359">-2146824560</span></span><br />
<span data-ttu-id="3568a-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="3568a-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="3568a-361">権限が不十分なために、ツリーまたはサブツリーにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="3568a-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-362"><strong>aderrunavailable 不可</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-363">3736</span><span class="sxs-lookup"><span data-stu-id="3568a-363">3736</span></span><br />
<span data-ttu-id="3568a-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="3568a-364">-2146824552</span></span><br />
<span data-ttu-id="3568a-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="3568a-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="3568a-366">操作の完了に失敗し、状態は利用できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-366">Operation failed to complete and the status is unavailable.</span></span> <span data-ttu-id="3568a-367">フィールドが利用できないか、操作が実行されなかった可能性があります。</span><span class="sxs-lookup"><span data-stu-id="3568a-367">The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-368"><strong>aderrアン safeoperation</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-369">3716</span><span class="sxs-lookup"><span data-stu-id="3568a-369">3716</span></span><br />
<span data-ttu-id="3568a-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="3568a-370">-2146824572</span></span><br />
<span data-ttu-id="3568a-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="3568a-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="3568a-372">このコンピューターの安全性の設定により、他のドメインのデータ ソースへのアクセスが禁止されています。</span><span class="sxs-lookup"><span data-stu-id="3568a-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-374">3727</span><span class="sxs-lookup"><span data-stu-id="3568a-374">3727</span></span><br />
<span data-ttu-id="3568a-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="3568a-375">-2146824561</span></span><br />
<span data-ttu-id="3568a-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="3568a-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="3568a-377">ソース URL または宛先の URL の親が存在しません。</span><span class="sxs-lookup"><span data-stu-id="3568a-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-379">3737</span><span class="sxs-lookup"><span data-stu-id="3568a-379">3737</span></span><br />
<span data-ttu-id="3568a-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="3568a-380">-2146824551</span></span><br />
<span data-ttu-id="3568a-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="3568a-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="3568a-382">この URL によって名前を付けられたレコードが存在しません。</span><span class="sxs-lookup"><span data-stu-id="3568a-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-383"><strong>aderrvolumenotfound</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-384">3733</span><span class="sxs-lookup"><span data-stu-id="3568a-384">3733</span></span><br />
<span data-ttu-id="3568a-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="3568a-385">-2146824555</span></span><br />
<span data-ttu-id="3568a-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="3568a-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="3568a-387">プロバイダーが、URL で示された記憶装置の場所を特定できません。</span><span class="sxs-lookup"><span data-stu-id="3568a-387">Provider cannot locate the storage device indicated by the URL.</span></span> <span data-ttu-id="3568a-388">URL が正しく入力されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="3568a-388">Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-389"><strong>aderrwritefile</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-390">3004</span><span class="sxs-lookup"><span data-stu-id="3568a-390">3004</span></span><br />
<span data-ttu-id="3568a-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="3568a-391">-2146825284</span></span><br />
<span data-ttu-id="3568a-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="3568a-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="3568a-393">ファイルへの書き込みに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="3568a-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-394"><strong>adwrnsecuritydialog</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-395">3717</span><span class="sxs-lookup"><span data-stu-id="3568a-395">3717</span></span><br />
<span data-ttu-id="3568a-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="3568a-396">-2146824571</span></span><br />
<span data-ttu-id="3568a-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="3568a-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="3568a-398">内部使用のために用意されています。</span><span class="sxs-lookup"><span data-stu-id="3568a-398">For internal use only.</span></span> <span data-ttu-id="3568a-399">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3568a-399">Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-400"><strong>adwrnsecuritydialogheader</strong></span><span class="sxs-lookup"><span data-stu-id="3568a-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="3568a-401">3718</span><span class="sxs-lookup"><span data-stu-id="3568a-401">3718</span></span><br />
<span data-ttu-id="3568a-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="3568a-402">-2146824570</span></span><br />
<span data-ttu-id="3568a-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="3568a-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="3568a-404">内部使用のために用意されています。</span><span class="sxs-lookup"><span data-stu-id="3568a-404">For internal use only.</span></span> <span data-ttu-id="3568a-405">使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="3568a-405">Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3568a-406">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="3568a-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="3568a-407">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3568a-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="3568a-408">次の ADO/WFC 等価のサブセットのみを定義します。</span><span class="sxs-lookup"><span data-stu-id="3568a-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3568a-409">定数</span><span class="sxs-lookup"><span data-stu-id="3568a-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3568a-410">AdoEnums tocommand を指定します。</span><span class="sxs-lookup"><span data-stu-id="3568a-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-411">AdoEnums DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="3568a-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-412">AdoEnums FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="3568a-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-413">AdoEnums ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="3568a-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-414">AdoEnums を指定します。 intransaction</span><span class="sxs-lookup"><span data-stu-id="3568a-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-415">AdoEnums INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="3568a-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-416">AdoEnums connection。 invalidconnection</span><span class="sxs-lookup"><span data-stu-id="3568a-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-417">AdoEnums の値を取得します。 invalidparaminfo</span><span class="sxs-lookup"><span data-stu-id="3568a-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-418">AdoEnums ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="3568a-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-419">AdoEnums NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="3568a-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-420">AdoEnums の実行</span><span class="sxs-lookup"><span data-stu-id="3568a-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-421">AdoEnums。 notreentrant</span><span class="sxs-lookup"><span data-stu-id="3568a-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-422">AdoEnums closed。</span><span class="sxs-lookup"><span data-stu-id="3568a-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-423">AdoEnums/オブジェクトのコレクション</span><span class="sxs-lookup"><span data-stu-id="3568a-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-424">AdoEnums の値がありません。</span><span class="sxs-lookup"><span data-stu-id="3568a-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-425">AdoEnums ado</span><span class="sxs-lookup"><span data-stu-id="3568a-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-426">AdoEnums が取り消されました</span><span class="sxs-lookup"><span data-stu-id="3568a-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-427">AdoEnums PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="3568a-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-428">AdoEnums STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="3568a-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3568a-429">AdoEnums STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="3568a-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3568a-430">AdoEnums の取り消し操作</span><span class="sxs-lookup"><span data-stu-id="3568a-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

