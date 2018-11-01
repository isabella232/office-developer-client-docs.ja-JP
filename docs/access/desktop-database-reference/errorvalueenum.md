---
title: ErrorValueEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ErrorValueEnum
ms:assetid: 2af99f32-6004-1225-367c-45d693f447b8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249058(v=office.15)
ms:contentKeyID: 48543921
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 23040dd7311d659fb5e3308053a3bcdc8aa27fe0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879866"
---
# <a name="errorvalueenum"></a><span data-ttu-id="9c14b-102">ErrorValueEnum</span><span class="sxs-lookup"><span data-stu-id="9c14b-102">ErrorValueEnum</span></span>

<span data-ttu-id="9c14b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="9c14b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9c14b-104">ADO 実行時エラーの種類を表します。</span><span class="sxs-lookup"><span data-stu-id="9c14b-104">Specifies the type of ADO run-time error.</span></span>

<span data-ttu-id="9c14b-105">エラー番号には次の 3 種類の形式があります。</span><span class="sxs-lookup"><span data-stu-id="9c14b-105">Three forms of the error number are listed:</span></span>

- <span data-ttu-id="9c14b-p101">正の 10 進値: 10 進数で表された完全エラー番号の下位 2 バイト。この数値は、Visual Basic の既定のエラー メッセージ ダイアログ ボックスに表示されます。たとえば、実行時エラー '3707' がその例です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p101">Positive decimal — the low two bytes of the full number in decimal format. This number is displayed in the default Visual Basic error message dialog box. For example, Run-time error '3707'.</span></span>

- <span data-ttu-id="9c14b-109">負の 10 進値: 完全エラー番号を 10 進数に変換したもの。</span><span class="sxs-lookup"><span data-stu-id="9c14b-109">Negative decimal — The decimal translation of the full error number.</span></span>

- <span data-ttu-id="9c14b-p102">16 進値: 完全エラー番号の 16 進数表記。Windows 機能コードは 4 桁目です。ADO エラー番号の機能コードは、*A* です。たとえば、0x800***A***0E7B がその例です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p102">Hexadecimal — The hexadecimal representation of the full error number. The Windows facility code is in the fourth digit. The facility code for ADO error numbers is *A*. For example: 0x800***A***0E7B.</span></span>

> [!NOTE]
> <span data-ttu-id="9c14b-113">OLE DB エラーは、ADO アプリケーションに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="9c14b-113">OLE DB errors may be passed to your ADO application.</span></span> <span data-ttu-id="9c14b-114">通常、これらは*4*の Windows 機能コードで識別できます。</span><span class="sxs-lookup"><span data-stu-id="9c14b-114">Typically, these can be identified by a Windows facility code of *4*.</span></span> <span data-ttu-id="9c14b-115">たとえば、0x800_**4**_.これらの数値の詳細については、の第 16 章を参照してください、 *OLE DB プログラマ リファレンスです*。</span><span class="sxs-lookup"><span data-stu-id="9c14b-115">For example, 0x800_**4**_.... For more information about these numbers, see Chapter 16 of the *OLE DB Programmer's Reference.*</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c14b-116">定数</span><span class="sxs-lookup"><span data-stu-id="9c14b-116">Constant</span></span></p></th>
<th><p><span data-ttu-id="9c14b-117">値</span><span class="sxs-lookup"><span data-stu-id="9c14b-117">Value</span></span></p></th>
<th><p><span data-ttu-id="9c14b-118">説明</span><span class="sxs-lookup"><span data-stu-id="9c14b-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-119"><strong>adErrBoundToCommand</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-119"><strong>adErrBoundToCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-120">3707</span><span class="sxs-lookup"><span data-stu-id="9c14b-120">3707</span></span><br />
<span data-ttu-id="9c14b-121">-2146824581</span><span class="sxs-lookup"><span data-stu-id="9c14b-121">-2146824581</span></span><br />
<span data-ttu-id="9c14b-122">0x800A0E7B</span><span class="sxs-lookup"><span data-stu-id="9c14b-122">0x800A0E7B</span></span></p></td>
<td><p><span data-ttu-id="9c14b-123"><strong>Command</strong> オブジェクトをソースに持つ <strong>Recordset</strong> オブジェクトの <strong>ActiveConnection</strong> プロパティを変更できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-123">Cannot change the <strong>ActiveConnection</strong> property of a <strong>Recordset</strong> object which has a <strong>Command</strong> object as its source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-124"><strong>adErrCannotComplete</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-124"><strong>adErrCannotComplete</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-125">3732</span><span class="sxs-lookup"><span data-stu-id="9c14b-125">3732</span></span><br />
<span data-ttu-id="9c14b-126">-2146824556</span><span class="sxs-lookup"><span data-stu-id="9c14b-126">-2146824556</span></span><br />
<span data-ttu-id="9c14b-127">0x800A0E94</span><span class="sxs-lookup"><span data-stu-id="9c14b-127">0x800A0E94</span></span></p></td>
<td><p><span data-ttu-id="9c14b-128">サーバーは操作を完了できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-128">Server cannot complete the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-129"><strong>adErrCantChangeConnection</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-129"><strong>adErrCantChangeConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-130">3748</span><span class="sxs-lookup"><span data-stu-id="9c14b-130">3748</span></span><br />
<span data-ttu-id="9c14b-131">-2146824540</span><span class="sxs-lookup"><span data-stu-id="9c14b-131">-2146824540</span></span><br />
<span data-ttu-id="9c14b-132">0x800A0EA4</span><span class="sxs-lookup"><span data-stu-id="9c14b-132">0x800A0EA4</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p104">接続が拒否されました。要求された新規接続の特性が現在使用中の特性と異なります。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p104">Connection was denied. New connection you requested has different characteristics than the one already in use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-135"><strong>adErrCantChangeProvider</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-135"><strong>adErrCantChangeProvider</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-136">3220</span><span class="sxs-lookup"><span data-stu-id="9c14b-136">3220</span></span><br />
<span data-ttu-id="9c14b-137">-2146825068</span><span class="sxs-lookup"><span data-stu-id="9c14b-137">-2146825068</span></span><br />
<span data-ttu-id="9c14b-138">0X800A0C94</span><span class="sxs-lookup"><span data-stu-id="9c14b-138">0X800A0C94</span></span></p></td>
<td><p><span data-ttu-id="9c14b-139">指定されたプロバイダーが既に使用されているものと異なります。</span><span class="sxs-lookup"><span data-stu-id="9c14b-139">Supplied provider is different from the one already in use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-140"><strong>adErrCantConvertvalue</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-140"><strong>adErrCantConvertvalue</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-141">3724</span><span class="sxs-lookup"><span data-stu-id="9c14b-141">3724</span></span><br />
<span data-ttu-id="9c14b-142">-2146824564</span><span class="sxs-lookup"><span data-stu-id="9c14b-142">-2146824564</span></span><br />
<span data-ttu-id="9c14b-143">0x800A0E8C</span><span class="sxs-lookup"><span data-stu-id="9c14b-143">0x800A0E8C</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p105">符号の不一致またはデータ オーバーフロー以外の理由により、データ値を変換できません。たとえば、変換によりデータの一部が切り捨てられる場合などです。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p105">Data value cannot be converted for reasons other than sign mismatch or data overflow. For example, conversion would have truncated data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-146"><strong>adErrCantCreate</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-146"><strong>adErrCantCreate</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-147">3725</span><span class="sxs-lookup"><span data-stu-id="9c14b-147">3725</span></span><br />
<span data-ttu-id="9c14b-148">-2146824563</span><span class="sxs-lookup"><span data-stu-id="9c14b-148">-2146824563</span></span><br />
<span data-ttu-id="9c14b-149">0x800A0E8D</span><span class="sxs-lookup"><span data-stu-id="9c14b-149">0x800A0E8D</span></span></p></td>
<td><p><span data-ttu-id="9c14b-150">フィールドのデータ型が不明であったか、プロバイダーが操作を実行するのに十分なリソースを持っていなかったため、データ値を設定または取得できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-150">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-151"><strong>adErrCatalogNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-151"><strong>adErrCatalogNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-152">3747</span><span class="sxs-lookup"><span data-stu-id="9c14b-152">3747</span></span><br />
<span data-ttu-id="9c14b-153">-2146824541</span><span class="sxs-lookup"><span data-stu-id="9c14b-153">-2146824541</span></span><br />
<span data-ttu-id="9c14b-154">0x800A0EA3</span><span class="sxs-lookup"><span data-stu-id="9c14b-154">0x800A0EA3</span></span></p></td>
<td><p><span data-ttu-id="9c14b-155">操作には有効な <strong>ParentCatalog</strong> が必要です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-155">Operation requires a valid <strong>ParentCatalog</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-156"><strong>adErrColumnNotOnThisRow</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-156"><strong>adErrColumnNotOnThisRow</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-157">3726</span><span class="sxs-lookup"><span data-stu-id="9c14b-157">3726</span></span><br />
<span data-ttu-id="9c14b-158">-2146824562</span><span class="sxs-lookup"><span data-stu-id="9c14b-158">-2146824562</span></span><br />
<span data-ttu-id="9c14b-159">0x800A0E8E</span><span class="sxs-lookup"><span data-stu-id="9c14b-159">0x800A0E8E</span></span></p></td>
<td><p><span data-ttu-id="9c14b-160">レコードにこのフィールドが存在しません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-160">Record does not contain this field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-161"><strong>adErrDataConversion</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-161"><strong>adErrDataConversion</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-162">3421</span><span class="sxs-lookup"><span data-stu-id="9c14b-162">3421</span></span><br />
<span data-ttu-id="9c14b-163">-2146824867</span><span class="sxs-lookup"><span data-stu-id="9c14b-163">-2146824867</span></span><br />
<span data-ttu-id="9c14b-164">0x800A0D5D</span><span class="sxs-lookup"><span data-stu-id="9c14b-164">0x800A0D5D</span></span></p></td>
<td><p><span data-ttu-id="9c14b-165">現在の操作に対して、アプリケーションが間違った型の値を使用しています。</span><span class="sxs-lookup"><span data-stu-id="9c14b-165">Application uses a value of the wrong type for the current operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-166"><strong>adErrDataOverflow</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-166"><strong>adErrDataOverflow</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-167">3721</span><span class="sxs-lookup"><span data-stu-id="9c14b-167">3721</span></span><br />
<span data-ttu-id="9c14b-168">-2146824567</span><span class="sxs-lookup"><span data-stu-id="9c14b-168">-2146824567</span></span><br />
<span data-ttu-id="9c14b-169">0x800A0E89</span><span class="sxs-lookup"><span data-stu-id="9c14b-169">0x800A0E89</span></span></p></td>
<td><p><span data-ttu-id="9c14b-170">データ値が大きすぎるために、フィールドのデータ型で表現できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-170">Data value is too large to be represented by the field data type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-171"><strong>adErrDelResOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-171"><strong>adErrDelResOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-172">3738</span><span class="sxs-lookup"><span data-stu-id="9c14b-172">3738</span></span><br />
<span data-ttu-id="9c14b-173">-2146824550</span><span class="sxs-lookup"><span data-stu-id="9c14b-173">-2146824550</span></span><br />
<span data-ttu-id="9c14b-174">0x800A0E9A</span><span class="sxs-lookup"><span data-stu-id="9c14b-174">0x800A0E9A</span></span></p></td>
<td><p><span data-ttu-id="9c14b-175">削除されるオブジェクトの URL は現在のレコードの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-175">URL of the object to be deleted is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-176"><strong>adErrDenyNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-176"><strong>adErrDenyNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-177">3750</span><span class="sxs-lookup"><span data-stu-id="9c14b-177">3750</span></span><br />
<span data-ttu-id="9c14b-178">-2146824538</span><span class="sxs-lookup"><span data-stu-id="9c14b-178">-2146824538</span></span><br />
<span data-ttu-id="9c14b-179">0x800A0EA6</span><span class="sxs-lookup"><span data-stu-id="9c14b-179">0x800A0EA6</span></span></p></td>
<td><p><span data-ttu-id="9c14b-180">プロバイダーが共有の制約をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-180">Provider does not support sharing restrictions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-181"><strong>adErrDenyTypeNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-181"><strong>adErrDenyTypeNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-182">3751</span><span class="sxs-lookup"><span data-stu-id="9c14b-182">3751</span></span><br />
<span data-ttu-id="9c14b-183">-2146824537</span><span class="sxs-lookup"><span data-stu-id="9c14b-183">-2146824537</span></span><br />
<span data-ttu-id="9c14b-184">0x800A0EA7</span><span class="sxs-lookup"><span data-stu-id="9c14b-184">0x800A0EA7</span></span></p></td>
<td><p><span data-ttu-id="9c14b-185">プロバイダーが、要求された種類の共有の制約をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-185">Provider does not support the requested kind of sharing restriction.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-186"><strong>adErrFeatureNotAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-186"><strong>adErrFeatureNotAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-187">3251</span><span class="sxs-lookup"><span data-stu-id="9c14b-187">3251</span></span><br />
<span data-ttu-id="9c14b-188">-2146825037</span><span class="sxs-lookup"><span data-stu-id="9c14b-188">-2146825037</span></span><br />
<span data-ttu-id="9c14b-189">0x800A0CB3</span><span class="sxs-lookup"><span data-stu-id="9c14b-189">0x800A0CB3</span></span></p></td>
<td><p><span data-ttu-id="9c14b-190">オブジェクトまたはプロバイダーは要求された操作を実行できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-190">Object or provider is not capable of performing requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-191"><strong>adErrFieldsUpdateFailed</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-191"><strong>adErrFieldsUpdateFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-192">3749</span><span class="sxs-lookup"><span data-stu-id="9c14b-192">3749</span></span><br />
<span data-ttu-id="9c14b-193">-2146824539</span><span class="sxs-lookup"><span data-stu-id="9c14b-193">-2146824539</span></span><br />
<span data-ttu-id="9c14b-194">0x800A0EA5</span><span class="sxs-lookup"><span data-stu-id="9c14b-194">0x800A0EA5</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p106">フィールドの更新に失敗しました。詳細については、各 Field オブジェクトの <strong>Status</strong> プロパティを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p106">Fields update failed. For further information, examine the <strong>Status</strong> property of individual field objects.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-197"><strong>adErrIllegalOperation</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-197"><strong>adErrIllegalOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-198">3219</span><span class="sxs-lookup"><span data-stu-id="9c14b-198">3219</span></span><br />
<span data-ttu-id="9c14b-199">-2146825069</span><span class="sxs-lookup"><span data-stu-id="9c14b-199">-2146825069</span></span><br />
<span data-ttu-id="9c14b-200">0x800A0C93</span><span class="sxs-lookup"><span data-stu-id="9c14b-200">0x800A0C93</span></span></p></td>
<td><p><span data-ttu-id="9c14b-201">このコンテキストで操作は許可されていません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-201">Operation is not allowed in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-202"><strong>adErrIntegrityViolation</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-202"><strong>adErrIntegrityViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-203">3719</span><span class="sxs-lookup"><span data-stu-id="9c14b-203">3719</span></span><br />
<span data-ttu-id="9c14b-204">-2146824569</span><span class="sxs-lookup"><span data-stu-id="9c14b-204">-2146824569</span></span><br />
<span data-ttu-id="9c14b-205">0x800A0E87</span><span class="sxs-lookup"><span data-stu-id="9c14b-205">0x800A0E87</span></span></p></td>
<td><p><span data-ttu-id="9c14b-206">データ値がフィールドの整合性制約に反しています。</span><span class="sxs-lookup"><span data-stu-id="9c14b-206">Data value conflicts with the integrity constraints of the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-207"><strong>adErrInTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-207"><strong>adErrInTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-208">3246</span><span class="sxs-lookup"><span data-stu-id="9c14b-208">3246</span></span><br />
<span data-ttu-id="9c14b-209">-2146825042</span><span class="sxs-lookup"><span data-stu-id="9c14b-209">-2146825042</span></span><br />
<span data-ttu-id="9c14b-210">0x800A0CAE</span><span class="sxs-lookup"><span data-stu-id="9c14b-210">0x800A0CAE</span></span></p></td>
<td><p><span data-ttu-id="9c14b-211">トランザクションの実行中に <strong>Connection</strong> オブジェクトを明示的に閉じることができません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-211"><strong>Connection</strong> object cannot be explicitly closed while in a transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-212"><strong>adErrInvalidArgument</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-212"><strong>adErrInvalidArgument</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-213">3001</span><span class="sxs-lookup"><span data-stu-id="9c14b-213">3001</span></span><br />
<span data-ttu-id="9c14b-214">-2146825287</span><span class="sxs-lookup"><span data-stu-id="9c14b-214">-2146825287</span></span><br />
<span data-ttu-id="9c14b-215">0x800A0BB9</span><span class="sxs-lookup"><span data-stu-id="9c14b-215">0x800A0BB9</span></span></p></td>
<td><p><span data-ttu-id="9c14b-216">間違った種類または許容範囲外の引数を使用しているか、使用している引数が競合しています。</span><span class="sxs-lookup"><span data-stu-id="9c14b-216">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-217"><strong>adErrInvalidConnection</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-217"><strong>adErrInvalidConnection</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-218">3709</span><span class="sxs-lookup"><span data-stu-id="9c14b-218">3709</span></span><br />
<span data-ttu-id="9c14b-219">-2146824579</span><span class="sxs-lookup"><span data-stu-id="9c14b-219">-2146824579</span></span><br />
<span data-ttu-id="9c14b-220">0x800A0E7D</span><span class="sxs-lookup"><span data-stu-id="9c14b-220">0x800A0E7D</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p107">この操作を実行するために接続を使用できません。このコンテキストで閉じているかあるいは無効です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p107">The connection cannot be used to perform this operation. It is either closed or invalid in this context.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-223"><strong>adErrInvalidParamInfo</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-223"><strong>adErrInvalidParamInfo</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-224">3708</span><span class="sxs-lookup"><span data-stu-id="9c14b-224">3708</span></span><br />
<span data-ttu-id="9c14b-225">-2146824580</span><span class="sxs-lookup"><span data-stu-id="9c14b-225">-2146824580</span></span><br />
<span data-ttu-id="9c14b-226">0x800A0E7C</span><span class="sxs-lookup"><span data-stu-id="9c14b-226">0x800A0E7C</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p108"><strong>Parameter</strong> オブジェクトが適切に定義されていません。矛盾した、または不完全な情報が指定されました。  </span><span class="sxs-lookup"><span data-stu-id="9c14b-p108"><strong>Parameter</strong> object is improperly defined. Inconsistent or incomplete information was provided.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-229"><strong>adErrInvalidTransaction</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-229"><strong>adErrInvalidTransaction</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-230">3714</span><span class="sxs-lookup"><span data-stu-id="9c14b-230">3714</span></span><br />
<span data-ttu-id="9c14b-231">-2146824574</span><span class="sxs-lookup"><span data-stu-id="9c14b-231">-2146824574</span></span><br />
<span data-ttu-id="9c14b-232">0x800A0E82</span><span class="sxs-lookup"><span data-stu-id="9c14b-232">0x800A0E82</span></span></p></td>
<td><p><span data-ttu-id="9c14b-233">調整トランザクションが無効であるか、開始されていません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-233">Coordinating transaction is invalid or has not started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-234"><strong>adErrInvalidURL</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-234"><strong>adErrInvalidURL</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-235">3729</span><span class="sxs-lookup"><span data-stu-id="9c14b-235">3729</span></span><br />
<span data-ttu-id="9c14b-236">-2146824559</span><span class="sxs-lookup"><span data-stu-id="9c14b-236">-2146824559</span></span><br />
<span data-ttu-id="9c14b-237">0x800A0E91</span><span class="sxs-lookup"><span data-stu-id="9c14b-237">0x800A0E91</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p109">URL に無効な文字が含まれています。URL が正しく入力されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p109">URL contains invalid characters. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-240"><strong>adErrItemNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-240"><strong>adErrItemNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-241">3265</span><span class="sxs-lookup"><span data-stu-id="9c14b-241">3265</span></span><br />
<span data-ttu-id="9c14b-242">-2146825023</span><span class="sxs-lookup"><span data-stu-id="9c14b-242">-2146825023</span></span><br />
<span data-ttu-id="9c14b-243">0x800a0cc1 が</span><span class="sxs-lookup"><span data-stu-id="9c14b-243">0x800A0CC1</span></span></p></td>
<td><p><span data-ttu-id="9c14b-244">要求された名前、または序数に対応する項目がコレクションで見つかりません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-244">Item cannot be found in the collection corresponding to the requested name or ordinal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-245"><strong>adErrNoCurrentRecord</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-245"><strong>adErrNoCurrentRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-246">3021</span><span class="sxs-lookup"><span data-stu-id="9c14b-246">3021</span></span><br />
<span data-ttu-id="9c14b-247">-2146825267</span><span class="sxs-lookup"><span data-stu-id="9c14b-247">-2146825267</span></span><br />
<span data-ttu-id="9c14b-248">0x800A0BCD</span><span class="sxs-lookup"><span data-stu-id="9c14b-248">0x800A0BCD</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p110"><strong>BOF</strong> または <strong>EOF</strong> が True であるか、現在のレコードが削除されています。要求された操作には現在のレコードが必要です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p110">Either <strong>BOF</strong> or <strong>EOF</strong> is True, or the current record has been deleted. Requested operation requires a current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-251"><strong>adErrNotExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-251"><strong>adErrNotExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-252">3715</span><span class="sxs-lookup"><span data-stu-id="9c14b-252">3715</span></span><br />
<span data-ttu-id="9c14b-253">-2146824573</span><span class="sxs-lookup"><span data-stu-id="9c14b-253">-2146824573</span></span><br />
<span data-ttu-id="9c14b-254">0x800A0E83</span><span class="sxs-lookup"><span data-stu-id="9c14b-254">0x800A0E83</span></span></p></td>
<td><p><span data-ttu-id="9c14b-255">実行していない間に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-255">Operation cannot be performed while not executing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-256"><strong>adErrNotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-256"><strong>adErrNotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-257">3710</span><span class="sxs-lookup"><span data-stu-id="9c14b-257">3710</span></span><br />
<span data-ttu-id="9c14b-258">-2146824578</span><span class="sxs-lookup"><span data-stu-id="9c14b-258">-2146824578</span></span><br />
<span data-ttu-id="9c14b-259">0x800A0E7E</span><span class="sxs-lookup"><span data-stu-id="9c14b-259">0x800A0E7E</span></span></p></td>
<td><p><span data-ttu-id="9c14b-260">イベント処理中に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-260">Operation cannot be performed while processing event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-261"><strong>adErrObjectClosed</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-261"><strong>adErrObjectClosed</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-262">3704</span><span class="sxs-lookup"><span data-stu-id="9c14b-262">3704</span></span><br />
<span data-ttu-id="9c14b-263">-2146824584</span><span class="sxs-lookup"><span data-stu-id="9c14b-263">-2146824584</span></span><br />
<span data-ttu-id="9c14b-264">0x800A0E78</span><span class="sxs-lookup"><span data-stu-id="9c14b-264">0x800A0E78</span></span></p></td>
<td><p><span data-ttu-id="9c14b-265">オブジェクトが閉じている場合は、操作は許可されません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-265">Operation is not allowed when the object is closed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-266"><strong>adErrObjectInCollection</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-266"><strong>adErrObjectInCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-267">3367</span><span class="sxs-lookup"><span data-stu-id="9c14b-267">3367</span></span><br />
<span data-ttu-id="9c14b-268">-2146824921</span><span class="sxs-lookup"><span data-stu-id="9c14b-268">-2146824921</span></span><br />
<span data-ttu-id="9c14b-269">0x800A0D27</span><span class="sxs-lookup"><span data-stu-id="9c14b-269">0x800A0D27</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p111">オブジェクトは既にコレクションに存在します。追加できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p111">Object is already in collection. Cannot append.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-272"><strong>adErrObjectNotSet</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-272"><strong>adErrObjectNotSet</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-273">3420</span><span class="sxs-lookup"><span data-stu-id="9c14b-273">3420</span></span><br />
<span data-ttu-id="9c14b-274">-2146824868</span><span class="sxs-lookup"><span data-stu-id="9c14b-274">-2146824868</span></span><br />
<span data-ttu-id="9c14b-275">0x800A0D5C</span><span class="sxs-lookup"><span data-stu-id="9c14b-275">0x800A0D5C</span></span></p></td>
<td><p><span data-ttu-id="9c14b-276">オブジェクトが無効になっています。</span><span class="sxs-lookup"><span data-stu-id="9c14b-276">Object is no longer valid.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-277"><strong>adErrObjectOpen</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-277"><strong>adErrObjectOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-278">3705</span><span class="sxs-lookup"><span data-stu-id="9c14b-278">3705</span></span><br />
<span data-ttu-id="9c14b-279">-2146824583</span><span class="sxs-lookup"><span data-stu-id="9c14b-279">-2146824583</span></span><br />
<span data-ttu-id="9c14b-280">0x800A0E79</span><span class="sxs-lookup"><span data-stu-id="9c14b-280">0x800A0E79</span></span></p></td>
<td><p><span data-ttu-id="9c14b-281">オブジェクトが開いている場合は、操作は許可されません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-281">Operation is not allowed when the object is open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-282"><strong>adErrOpeningFile</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-282"><strong>adErrOpeningFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-283">3002</span><span class="sxs-lookup"><span data-stu-id="9c14b-283">3002</span></span><br />
<span data-ttu-id="9c14b-284">-2146825286</span><span class="sxs-lookup"><span data-stu-id="9c14b-284">-2146825286</span></span><br />
<span data-ttu-id="9c14b-285">0x800A0BBA</span><span class="sxs-lookup"><span data-stu-id="9c14b-285">0x800A0BBA</span></span></p></td>
<td><p><span data-ttu-id="9c14b-286">ファイルを開くことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="9c14b-286">File could not be opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-287"><strong>adErrOperationCancelled</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-287"><strong>adErrOperationCancelled</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-288">3712</span><span class="sxs-lookup"><span data-stu-id="9c14b-288">3712</span></span><br />
<span data-ttu-id="9c14b-289">-2146824576</span><span class="sxs-lookup"><span data-stu-id="9c14b-289">-2146824576</span></span><br />
<span data-ttu-id="9c14b-290">0x800A0E80</span><span class="sxs-lookup"><span data-stu-id="9c14b-290">0x800A0E80</span></span></p></td>
<td><p><span data-ttu-id="9c14b-291">ユーザーにより操作が取り消されました。</span><span class="sxs-lookup"><span data-stu-id="9c14b-291">Operation has been cancelled by the user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-292"><strong>adErrOutOfSpace</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-292"><strong>adErrOutOfSpace</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-293">3734</span><span class="sxs-lookup"><span data-stu-id="9c14b-293">3734</span></span><br />
<span data-ttu-id="9c14b-294">-2146824554</span><span class="sxs-lookup"><span data-stu-id="9c14b-294">-2146824554</span></span><br />
<span data-ttu-id="9c14b-295">0x800A0E96</span><span class="sxs-lookup"><span data-stu-id="9c14b-295">0x800A0E96</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p112">操作を実行できません。プロバイダーによって十分な記憶域が確保できません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p112">Operation cannot be performed. Provider cannot obtain enough storage space.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-298"><strong>adErrPermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-298"><strong>adErrPermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-299">3720</span><span class="sxs-lookup"><span data-stu-id="9c14b-299">3720</span></span><br />
<span data-ttu-id="9c14b-300">-2146824568</span><span class="sxs-lookup"><span data-stu-id="9c14b-300">-2146824568</span></span><br />
<span data-ttu-id="9c14b-301">0x800A0E88</span><span class="sxs-lookup"><span data-stu-id="9c14b-301">0x800A0E88</span></span></p></td>
<td><p><span data-ttu-id="9c14b-302">権限不足のためフィールドの書き込みはできません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-302">Insufficent permission prevents writing to the field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-303"><strong>adErrProviderFailed</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-303"><strong>adErrProviderFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-304">3000</span><span class="sxs-lookup"><span data-stu-id="9c14b-304">3000</span></span><br />
<span data-ttu-id="9c14b-305">-2146825288</span><span class="sxs-lookup"><span data-stu-id="9c14b-305">-2146825288</span></span><br />
<span data-ttu-id="9c14b-306">0x800A0BB8</span><span class="sxs-lookup"><span data-stu-id="9c14b-306">0x800A0BB8</span></span></p></td>
<td><p><span data-ttu-id="9c14b-307">プロバイダーが要求された操作を実行できませんでした。</span><span class="sxs-lookup"><span data-stu-id="9c14b-307">Provider failed to perform the requested operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-308"><strong>adErrProviderNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-308"><strong>adErrProviderNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-309">3706</span><span class="sxs-lookup"><span data-stu-id="9c14b-309">3706</span></span><br />
<span data-ttu-id="9c14b-310">-2146824582</span><span class="sxs-lookup"><span data-stu-id="9c14b-310">-2146824582</span></span><br />
<span data-ttu-id="9c14b-311">0x800A0E7A</span><span class="sxs-lookup"><span data-stu-id="9c14b-311">0x800A0E7A</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p113">プロバイダーが見つかりません。正しくインストールされていない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p113">Provider cannot be found. It may not be properly installed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-314"><strong>adErrReadFile</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-314"><strong>adErrReadFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-315">3003</span><span class="sxs-lookup"><span data-stu-id="9c14b-315">3003</span></span><br />
<span data-ttu-id="9c14b-316">-2146825285</span><span class="sxs-lookup"><span data-stu-id="9c14b-316">-2146825285</span></span><br />
<span data-ttu-id="9c14b-317">0x800A0BBB</span><span class="sxs-lookup"><span data-stu-id="9c14b-317">0x800A0BBB</span></span></p></td>
<td><p><span data-ttu-id="9c14b-318">ファイルを読み込むことができませんでした。</span><span class="sxs-lookup"><span data-stu-id="9c14b-318">File could not be read.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-319"><strong>adErrResourceExists</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-319"><strong>adErrResourceExists</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-320">3731</span><span class="sxs-lookup"><span data-stu-id="9c14b-320">3731</span></span><br />
<span data-ttu-id="9c14b-321">-2146824557</span><span class="sxs-lookup"><span data-stu-id="9c14b-321">-2146824557</span></span><br />
<span data-ttu-id="9c14b-322">0x800A0E93</span><span class="sxs-lookup"><span data-stu-id="9c14b-322">0x800A0E93</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p114">コピー操作を実行できません。宛先の URL によって名前を指定されたオブジェクトが既に存在します。オブジェクトを置き換えるためには <strong>adCopyOverwrite</strong> を指定してください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p114">Copy operation cannot be performed. Object named by destination URL already exists. Specify <strong>adCopyOverwrite</strong> to replace the object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-326"><strong>adErrResourceLocked</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-326"><strong>adErrResourceLocked</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-327">3730</span><span class="sxs-lookup"><span data-stu-id="9c14b-327">3730</span></span><br />
<span data-ttu-id="9c14b-328">-2146824558</span><span class="sxs-lookup"><span data-stu-id="9c14b-328">-2146824558</span></span><br />
<span data-ttu-id="9c14b-329">0x800A0E92</span><span class="sxs-lookup"><span data-stu-id="9c14b-329">0x800A0E92</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p115">指定された URL によって表されたオブジェクトは 1 つ以上の他のプロセスによってロックされています。プロセスが終了するまで待って、操作を再度実行してください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p115">Object represented by the specified URL is locked by one or more other processes. Wait until the process has finished and attempt the operation again.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-332"><strong>adErrResourceOutOfScope</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-332"><strong>adErrResourceOutOfScope</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-333">3735</span><span class="sxs-lookup"><span data-stu-id="9c14b-333">3735</span></span><br />
<span data-ttu-id="9c14b-334">-2146824553</span><span class="sxs-lookup"><span data-stu-id="9c14b-334">-2146824553</span></span><br />
<span data-ttu-id="9c14b-335">0x800A0E97</span><span class="sxs-lookup"><span data-stu-id="9c14b-335">0x800A0E97</span></span></p></td>
<td><p><span data-ttu-id="9c14b-336">ソースまたは宛先の URL が、現在のレコードの範囲外です。</span><span class="sxs-lookup"><span data-stu-id="9c14b-336">Source or destination URL is outside the scope of the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-337"><strong>adErrSchemaViolation</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-337"><strong>adErrSchemaViolation</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-338">3722</span><span class="sxs-lookup"><span data-stu-id="9c14b-338">3722</span></span><br />
<span data-ttu-id="9c14b-339">-2146824566</span><span class="sxs-lookup"><span data-stu-id="9c14b-339">-2146824566</span></span><br />
<span data-ttu-id="9c14b-340">0x800A0E8A</span><span class="sxs-lookup"><span data-stu-id="9c14b-340">0x800A0E8A</span></span></p></td>
<td><p><span data-ttu-id="9c14b-341">データ値がフィールドのデータ型と一致していないか、フィールドの制約に反しています。</span><span class="sxs-lookup"><span data-stu-id="9c14b-341">Data value conflicts with the data type or constraints of the field.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-342"><strong>adErrSignMismatch</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-342"><strong>adErrSignMismatch</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-343">3723</span><span class="sxs-lookup"><span data-stu-id="9c14b-343">3723</span></span><br />
<span data-ttu-id="9c14b-344">-2146824565</span><span class="sxs-lookup"><span data-stu-id="9c14b-344">-2146824565</span></span><br />
<span data-ttu-id="9c14b-345">0x800A0E8B</span><span class="sxs-lookup"><span data-stu-id="9c14b-345">0x800A0E8B</span></span></p></td>
<td><p><span data-ttu-id="9c14b-346">データの値は符号付きですが、プロバイダーによって使用されるフィールド データ型は符号なしのため、変換に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="9c14b-346">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-347"><strong>adErrStillConnecting</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-347"><strong>adErrStillConnecting</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-348">3713</span><span class="sxs-lookup"><span data-stu-id="9c14b-348">3713</span></span><br />
<span data-ttu-id="9c14b-349">-2146824575</span><span class="sxs-lookup"><span data-stu-id="9c14b-349">-2146824575</span></span><br />
<span data-ttu-id="9c14b-350">0x800A0E81</span><span class="sxs-lookup"><span data-stu-id="9c14b-350">0x800A0E81</span></span></p></td>
<td><p><span data-ttu-id="9c14b-351">非同期操作の保留中に、操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-351">Operation cannot be performed while connecting aynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-352"><strong>adErrStillExecuting</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-352"><strong>adErrStillExecuting</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-353">3711</span><span class="sxs-lookup"><span data-stu-id="9c14b-353">3711</span></span><br />
<span data-ttu-id="9c14b-354">-2146824577</span><span class="sxs-lookup"><span data-stu-id="9c14b-354">-2146824577</span></span><br />
<span data-ttu-id="9c14b-355">0x800A0E7F</span><span class="sxs-lookup"><span data-stu-id="9c14b-355">0x800A0E7F</span></span></p></td>
<td><p><span data-ttu-id="9c14b-356">非同期実行中に操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-356">Operation cannot be performed while executing asynchronously.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-357"><strong>adErrTreePermissionDenied</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-357"><strong>adErrTreePermissionDenied</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-358">3728</span><span class="sxs-lookup"><span data-stu-id="9c14b-358">3728</span></span><br />
<span data-ttu-id="9c14b-359">-2146824560</span><span class="sxs-lookup"><span data-stu-id="9c14b-359">-2146824560</span></span><br />
<span data-ttu-id="9c14b-360">0x800A0E90</span><span class="sxs-lookup"><span data-stu-id="9c14b-360">0x800A0E90</span></span></p></td>
<td><p><span data-ttu-id="9c14b-361">権限が不十分なために、ツリーまたはサブツリーにアクセスできません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-361">Permissions are insufficient to access tree or subtree.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-362"><strong>adErrUnavailable</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-362"><strong>adErrUnavailable</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-363">3736</span><span class="sxs-lookup"><span data-stu-id="9c14b-363">3736</span></span><br />
<span data-ttu-id="9c14b-364">-2146824552</span><span class="sxs-lookup"><span data-stu-id="9c14b-364">-2146824552</span></span><br />
<span data-ttu-id="9c14b-365">0x800A0E98</span><span class="sxs-lookup"><span data-stu-id="9c14b-365">0x800A0E98</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p116">操作の完了に失敗し、状態は利用できません。フィールドが利用できないか、操作が実行されなかった可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p116">Operation failed to complete and the status is unavailable. The field may be unavailable or the operation was not attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-368"><strong>adErrUnsafeOperation</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-368"><strong>adErrUnsafeOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-369">3716</span><span class="sxs-lookup"><span data-stu-id="9c14b-369">3716</span></span><br />
<span data-ttu-id="9c14b-370">-2146824572</span><span class="sxs-lookup"><span data-stu-id="9c14b-370">-2146824572</span></span><br />
<span data-ttu-id="9c14b-371">0x800A0E84</span><span class="sxs-lookup"><span data-stu-id="9c14b-371">0x800A0E84</span></span></p></td>
<td><p><span data-ttu-id="9c14b-372">このコンピューターの安全性の設定により、他のドメインのデータ ソースへのアクセスが禁止されています。</span><span class="sxs-lookup"><span data-stu-id="9c14b-372">Safety settings on this computer prohibit accessing a data source on another domain.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-373"><strong>adErrURLDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-373"><strong>adErrURLDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-374">3727</span><span class="sxs-lookup"><span data-stu-id="9c14b-374">3727</span></span><br />
<span data-ttu-id="9c14b-375">-2146824561</span><span class="sxs-lookup"><span data-stu-id="9c14b-375">-2146824561</span></span><br />
<span data-ttu-id="9c14b-376">0x800A0E8F</span><span class="sxs-lookup"><span data-stu-id="9c14b-376">0x800A0E8F</span></span></p></td>
<td><p><span data-ttu-id="9c14b-377">ソース URL または宛先の URL の親が存在しません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-377">Either the source URL or the parent of the destination URL does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-378"><strong>adErrURLNamedRowDoesNotExist</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-378"><strong>adErrURLNamedRowDoesNotExist</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-379">3737</span><span class="sxs-lookup"><span data-stu-id="9c14b-379">3737</span></span><br />
<span data-ttu-id="9c14b-380">-2146824551</span><span class="sxs-lookup"><span data-stu-id="9c14b-380">-2146824551</span></span><br />
<span data-ttu-id="9c14b-381">0x800A0E99</span><span class="sxs-lookup"><span data-stu-id="9c14b-381">0x800A0E99</span></span></p></td>
<td><p><span data-ttu-id="9c14b-382">この URL によって名前を付けられたレコードが存在しません。</span><span class="sxs-lookup"><span data-stu-id="9c14b-382">Record named by this URL does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-383"><strong>adErrVolumeNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-383"><strong>adErrVolumeNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-384">3733</span><span class="sxs-lookup"><span data-stu-id="9c14b-384">3733</span></span><br />
<span data-ttu-id="9c14b-385">-2146824555</span><span class="sxs-lookup"><span data-stu-id="9c14b-385">-2146824555</span></span><br />
<span data-ttu-id="9c14b-386">0x800A0E95</span><span class="sxs-lookup"><span data-stu-id="9c14b-386">0x800A0E95</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p117">プロバイダーは URL によって指定された記憶装置を見つけられません。URL が正しく入力されているか確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p117">Provider cannot locate the storage device indicated by the URL. Make sure the URL is typed correctly.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-389"><strong>adErrWriteFile</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-389"><strong>adErrWriteFile</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-390">3004</span><span class="sxs-lookup"><span data-stu-id="9c14b-390">3004</span></span><br />
<span data-ttu-id="9c14b-391">-2146825284</span><span class="sxs-lookup"><span data-stu-id="9c14b-391">-2146825284</span></span><br />
<span data-ttu-id="9c14b-392">0x800A0BBC</span><span class="sxs-lookup"><span data-stu-id="9c14b-392">0x800A0BBC</span></span></p></td>
<td><p><span data-ttu-id="9c14b-393">ファイルへの書き込みに失敗しました。</span><span class="sxs-lookup"><span data-stu-id="9c14b-393">Write to file failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-394"><strong>adWrnSecurityDialog</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-394"><strong>adWrnSecurityDialog</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-395">3717</span><span class="sxs-lookup"><span data-stu-id="9c14b-395">3717</span></span><br />
<span data-ttu-id="9c14b-396">-2146824571</span><span class="sxs-lookup"><span data-stu-id="9c14b-396">-2146824571</span></span><br />
<span data-ttu-id="9c14b-397">0x800A0E85</span><span class="sxs-lookup"><span data-stu-id="9c14b-397">0x800A0E85</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p118">内部使用のために用意されています。使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p118">For internal use only. Don't use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-400"><strong>adWrnSecurityDialogHeader</strong></span><span class="sxs-lookup"><span data-stu-id="9c14b-400"><strong>adWrnSecurityDialogHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="9c14b-401">3718</span><span class="sxs-lookup"><span data-stu-id="9c14b-401">3718</span></span><br />
<span data-ttu-id="9c14b-402">-2146824570</span><span class="sxs-lookup"><span data-stu-id="9c14b-402">-2146824570</span></span><br />
<span data-ttu-id="9c14b-403">0x800A0E86</span><span class="sxs-lookup"><span data-stu-id="9c14b-403">0x800A0E86</span></span></p></td>
<td><p><span data-ttu-id="9c14b-p119">内部使用のために用意されています。使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="9c14b-p119">For internal use only. Don't use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="9c14b-406">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="9c14b-406">ADO/WFC equivalent</span></span>

<span data-ttu-id="9c14b-407">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="9c14b-407">Package: **com.ms.wfc.data**</span></span>

<span data-ttu-id="9c14b-408">次の ADO/WFC 等価のサブセットのみを定義します。</span><span class="sxs-lookup"><span data-stu-id="9c14b-408">Only the following subsets of ADO/WFC equivalents are defined.</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9c14b-409">定数</span><span class="sxs-lookup"><span data-stu-id="9c14b-409">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span><span class="sxs-lookup"><span data-stu-id="9c14b-410">AdoEnums.ErrorValue.BOUNDTOCOMMAND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-411">AdoEnums.ErrorValue.DATACONVERSION</span><span class="sxs-lookup"><span data-stu-id="9c14b-411">AdoEnums.ErrorValue.DATACONVERSION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="9c14b-412">AdoEnums.ErrorValue.FEATURENOTAVAILABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span><span class="sxs-lookup"><span data-stu-id="9c14b-413">AdoEnums.ErrorValue.ILLEGALOPERATION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-414">AdoEnums.ErrorValue.INTRANSACTION</span><span class="sxs-lookup"><span data-stu-id="9c14b-414">AdoEnums.ErrorValue.INTRANSACTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span><span class="sxs-lookup"><span data-stu-id="9c14b-415">AdoEnums.ErrorValue.INVALIDARGUMENT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span><span class="sxs-lookup"><span data-stu-id="9c14b-416">AdoEnums.ErrorValue.INVALIDCONNECTION</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span><span class="sxs-lookup"><span data-stu-id="9c14b-417">AdoEnums.ErrorValue.INVALIDPARAMINFO</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="9c14b-418">AdoEnums.ErrorValue.ITEMNOTFOUND</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span><span class="sxs-lookup"><span data-stu-id="9c14b-419">AdoEnums.ErrorValue.NOCURRENTRECORD</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-420">AdoEnums.ErrorValue.NOTEXECUTING</span><span class="sxs-lookup"><span data-stu-id="9c14b-420">AdoEnums.ErrorValue.NOTEXECUTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-421">AdoEnums.ErrorValue.NOTREENTRANT</span><span class="sxs-lookup"><span data-stu-id="9c14b-421">AdoEnums.ErrorValue.NOTREENTRANT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-422">AdoEnums.ErrorValue.OBJECTCLOSED</span><span class="sxs-lookup"><span data-stu-id="9c14b-422">AdoEnums.ErrorValue.OBJECTCLOSED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span><span class="sxs-lookup"><span data-stu-id="9c14b-423">AdoEnums.ErrorValue.OBJECTINCOLLECTION</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-424">AdoEnums.ErrorValue.OBJECTNOTSET</span><span class="sxs-lookup"><span data-stu-id="9c14b-424">AdoEnums.ErrorValue.OBJECTNOTSET</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-425">AdoEnums.ErrorValue.OBJECTOPEN</span><span class="sxs-lookup"><span data-stu-id="9c14b-425">AdoEnums.ErrorValue.OBJECTOPEN</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span><span class="sxs-lookup"><span data-stu-id="9c14b-426">AdoEnums.ErrorValue.OPERATIONCANCELLED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span><span class="sxs-lookup"><span data-stu-id="9c14b-427">AdoEnums.ErrorValue.PROVIDERNOTFOUND</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-428">AdoEnums.ErrorValue.STILLCONNECTING</span><span class="sxs-lookup"><span data-stu-id="9c14b-428">AdoEnums.ErrorValue.STILLCONNECTING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c14b-429">AdoEnums.ErrorValue.STILLEXECUTING</span><span class="sxs-lookup"><span data-stu-id="9c14b-429">AdoEnums.ErrorValue.STILLEXECUTING</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c14b-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span><span class="sxs-lookup"><span data-stu-id="9c14b-430">AdoEnums.ErrorValue.UNSAFEOPERATION</span></span></p></td>
</tr>
</tbody>
</table>

