---
title: DataControl のエラー コード
TOCTitle: DataControl error codes
ms:assetid: d81446e2-aae6-b460-08a3-eae9920dc767
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250089(v=office.15)
ms:contentKeyID: 48548027
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 387f37e180d346c09cf3dadbf66f665cb83dbd0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294545"
---
# <a name="datacontrol-error-codes"></a><span data-ttu-id="7da00-102">DataControl のエラー コード</span><span class="sxs-lookup"><span data-stu-id="7da00-102">DataControl error codes</span></span>


<span data-ttu-id="7da00-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="7da00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7da00-p101">次の表は、[RDS.DataControl](datacontrol-object-rds.md) オブジェクトのエラー コードの一覧です。下位 2 バイトを正の 10 進数に変換した値、エラー コード全体を負の 10 進数に変換した値、および 16 進数値を示します。</span><span class="sxs-lookup"><span data-stu-id="7da00-p101">The following table lists the [RDS.DataControl](datacontrol-object-rds.md) object error codes. The positive decimal translation of the low two bytes, the negative decimal translation of the full error code, and the hexadecimal values are shown.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7da00-106">RDS.DataControl エラー コード</span><span class="sxs-lookup"><span data-stu-id="7da00-106">RDS.DataControl error codes</span></span></p></th>
<th><p><span data-ttu-id="7da00-107">番号</span><span class="sxs-lookup"><span data-stu-id="7da00-107">Number</span></span></p></th>
<th><p><span data-ttu-id="7da00-108">説明</span><span class="sxs-lookup"><span data-stu-id="7da00-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7da00-109"><strong>IDS_AsyncPending</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-109"><strong>IDS_AsyncPending</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-110">4107</span><span class="sxs-lookup"><span data-stu-id="7da00-110">4107</span></span><br />
<span data-ttu-id="7da00-111">-2146824175</span><span class="sxs-lookup"><span data-stu-id="7da00-111">-2146824175</span></span><br />
<span data-ttu-id="7da00-112">0x800a1011</span><span class="sxs-lookup"><span data-stu-id="7da00-112">0x800A1011</span></span></p></td>
<td><p><span data-ttu-id="7da00-113">非同期操作の保留中に、操作を行うことはできません。</span><span class="sxs-lookup"><span data-stu-id="7da00-113">Operation cannot be performed while async operation is pending.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-114"><strong>IDS_BadInlineTablegram</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-114"><strong>IDS_BadInlineTablegram</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-115">4105</span><span class="sxs-lookup"><span data-stu-id="7da00-115">4105</span></span><br />
<span data-ttu-id="7da00-116">-2146824183</span><span class="sxs-lookup"><span data-stu-id="7da00-116">-2146824183</span></span><br />
<span data-ttu-id="7da00-117">0x800a1009</span><span class="sxs-lookup"><span data-stu-id="7da00-117">0x800A1009</span></span></p></td>
<td><p><span data-ttu-id="7da00-118">インライン テーブルグラムが正しくありません。</span><span class="sxs-lookup"><span data-stu-id="7da00-118">Bad inline tablegram.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-119"><strong>IDS_CantConnect</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-119"><strong>IDS_CantConnect</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-120">4099</span><span class="sxs-lookup"><span data-stu-id="7da00-120">4099</span></span><br />
<span data-ttu-id="7da00-121">-2146824189</span><span class="sxs-lookup"><span data-stu-id="7da00-121">-2146824189</span></span><br />
<span data-ttu-id="7da00-122">0x800a1003</span><span class="sxs-lookup"><span data-stu-id="7da00-122">0x800A1003</span></span></p></td>
<td><p><span data-ttu-id="7da00-123">サーバーに接続できません。</span><span class="sxs-lookup"><span data-stu-id="7da00-123">Cannot connect to server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-124"><strong>IDS_CantCreateObject</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-124"><strong>IDS_CantCreateObject</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-125">4100</span><span class="sxs-lookup"><span data-stu-id="7da00-125">4100</span></span><br />
<span data-ttu-id="7da00-126">-2146824188</span><span class="sxs-lookup"><span data-stu-id="7da00-126">-2146824188</span></span><br />
<span data-ttu-id="7da00-127">0x800a1004</span><span class="sxs-lookup"><span data-stu-id="7da00-127">0x800A1004</span></span></p></td>
<td><p><span data-ttu-id="7da00-128">ビジネス オブジェクトは作成できません。</span><span class="sxs-lookup"><span data-stu-id="7da00-128">Business object cannot be created.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-129"><strong>IDS_CantFindDataspace</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-129"><strong>IDS_CantFindDataspace</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-130">4102</span><span class="sxs-lookup"><span data-stu-id="7da00-130">4102</span></span><br />
<span data-ttu-id="7da00-131">-2146824186</span><span class="sxs-lookup"><span data-stu-id="7da00-131">-2146824186</span></span><br />
<span data-ttu-id="7da00-132">0x800a1006</span><span class="sxs-lookup"><span data-stu-id="7da00-132">0x800A1006</span></span></p></td>
<td><p><span data-ttu-id="7da00-133">Dataspace プロパティは無効です。</span><span class="sxs-lookup"><span data-stu-id="7da00-133">Dataspace property is not valid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-134"><strong>IDS_CantInvokeMethod</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-134"><strong>IDS_CantInvokeMethod</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-135">4101</span><span class="sxs-lookup"><span data-stu-id="7da00-135">4101</span></span><br />
<span data-ttu-id="7da00-136">-2146824187</span><span class="sxs-lookup"><span data-stu-id="7da00-136">-2146824187</span></span><br />
<span data-ttu-id="7da00-137">0x800a1005</span><span class="sxs-lookup"><span data-stu-id="7da00-137">0x800A1005</span></span></p></td>
<td><p><span data-ttu-id="7da00-138">ビジネス オブジェクトのメソッドを呼び出せません。</span><span class="sxs-lookup"><span data-stu-id="7da00-138">Method cannot be invoked on business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-139"><strong>IDS_CrossDomainWarning</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-139"><strong>IDS_CrossDomainWarning</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-140">4112</span><span class="sxs-lookup"><span data-stu-id="7da00-140">4112</span></span><br />
<span data-ttu-id="7da00-141">-2146824170</span><span class="sxs-lookup"><span data-stu-id="7da00-141">-2146824170</span></span><br />
<span data-ttu-id="7da00-142">0x800a1016</span><span class="sxs-lookup"><span data-stu-id="7da00-142">0x800A1016</span></span></p></td>
<td><p><span data-ttu-id="7da00-143">このページは別のドメインにあるデータにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="7da00-143">This page accesses data on another domain.</span></span> <span data-ttu-id="7da00-144">このアクセスを許可してもよろしいですか?</span><span class="sxs-lookup"><span data-stu-id="7da00-144">Do you want to allow this?</span></span> <span data-ttu-id="7da00-145">internet Explorer でこのメッセージを表示しないようにするには、[<strong>インターネットオプション</strong>] ダイアログボックスの [<strong>セキュリティ</strong>] タブで、信頼済みサイトゾーンにセキュリティで保護された web サイトを追加します。</span><span class="sxs-lookup"><span data-stu-id="7da00-145">To avoid this message in Internet Explorer, you can add a secure website to your Trusted Sites zone on the <strong>Security</strong> tab of the <strong>Internet Options</strong> dialog box.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-146"><strong>IDS_InvalidADCClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-146"><strong>IDS_InvalidADCClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-147">4106</span><span class="sxs-lookup"><span data-stu-id="7da00-147">4106</span></span><br />
<span data-ttu-id="7da00-148">-2146824176</span><span class="sxs-lookup"><span data-stu-id="7da00-148">-2146824176</span></span><br />
<span data-ttu-id="7da00-149">0x800a1010</span><span class="sxs-lookup"><span data-stu-id="7da00-149">0x800A1010</span></span></p></td>
<td><p><span data-ttu-id="7da00-150">無効な RDS クライアントバージョン-クライアントはサーバーより新しいバージョンです。</span><span class="sxs-lookup"><span data-stu-id="7da00-150">Invalid RDS Client Version — Client is newer than server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-151"><strong>IDS_INVALIDARG</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-151"><strong>IDS_INVALIDARG</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-152">5376</span><span class="sxs-lookup"><span data-stu-id="7da00-152">5376</span></span><br />
<span data-ttu-id="7da00-153">-2147019520</span><span class="sxs-lookup"><span data-stu-id="7da00-153">-2147019520</span></span><br />
<span data-ttu-id="7da00-154">0x80071500</span><span class="sxs-lookup"><span data-stu-id="7da00-154">0x80071500</span></span></p></td>
<td><p><span data-ttu-id="7da00-155">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="7da00-155">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-156"><strong>IDS_InvalidBindings</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-156"><strong>IDS_InvalidBindings</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-157">4097</span><span class="sxs-lookup"><span data-stu-id="7da00-157">4097</span></span><br />
<span data-ttu-id="7da00-158">-2146824191</span><span class="sxs-lookup"><span data-stu-id="7da00-158">-2146824191</span></span><br />
<span data-ttu-id="7da00-159">0x800a1001</span><span class="sxs-lookup"><span data-stu-id="7da00-159">0x800A1001</span></span></p></td>
<td><p><span data-ttu-id="7da00-160">プロパティのバインド エラーです。</span><span class="sxs-lookup"><span data-stu-id="7da00-160">Error in bindings property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-161"><strong>IDS_InvalidParam</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-161"><strong>IDS_InvalidParam</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-162">4110</span><span class="sxs-lookup"><span data-stu-id="7da00-162">4110</span></span><br />
<span data-ttu-id="7da00-163">-2146824172</span><span class="sxs-lookup"><span data-stu-id="7da00-163">-2146824172</span></span><br />
<span data-ttu-id="7da00-164">0x800a1014</span><span class="sxs-lookup"><span data-stu-id="7da00-164">0x800A1014</span></span></p></td>
<td><p><span data-ttu-id="7da00-165">いくつかの引数は無効です。</span><span class="sxs-lookup"><span data-stu-id="7da00-165">One or more arguments are invalid.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-166"><strong>IDS_NOINTERFACE</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-166"><strong>IDS_NOINTERFACE</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-167">5377</span><span class="sxs-lookup"><span data-stu-id="7da00-167">5377</span></span><br />
<span data-ttu-id="7da00-168">-2147019519</span><span class="sxs-lookup"><span data-stu-id="7da00-168">-2147019519</span></span><br />
<span data-ttu-id="7da00-169">0x80071501</span><span class="sxs-lookup"><span data-stu-id="7da00-169">0x80071501</span></span></p></td>
<td><p><span data-ttu-id="7da00-170">そのインターフェイスはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="7da00-170">No such interface is supported.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-171"><strong>IDS_NotReentrant</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-171"><strong>IDS_NotReentrant</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-172">4111</span><span class="sxs-lookup"><span data-stu-id="7da00-172">4111</span></span><br />
<span data-ttu-id="7da00-173">-2146824171</span><span class="sxs-lookup"><span data-stu-id="7da00-173">-2146824171</span></span><br />
<span data-ttu-id="7da00-174">0x800a1015</span><span class="sxs-lookup"><span data-stu-id="7da00-174">0x800A1015</span></span></p></td>
<td><p><span data-ttu-id="7da00-175">イベント ハンドラーの処理中に要求を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="7da00-175">Request cannot be executed while the event handler is still processing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-176"><strong>IDS_ObjectNotSafe</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-176"><strong>IDS_ObjectNotSafe</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-177">4103</span><span class="sxs-lookup"><span data-stu-id="7da00-177">4103</span></span><br />
<span data-ttu-id="7da00-178">-2146824185</span><span class="sxs-lookup"><span data-stu-id="7da00-178">-2146824185</span></span><br />
<span data-ttu-id="7da00-179">0x800a1007</span><span class="sxs-lookup"><span data-stu-id="7da00-179">0x800A1007</span></span></p></td>
<td><p><span data-ttu-id="7da00-180">このコンピューターの安全性の設定により、ビジネス オブジェクトの作成が禁止されています。</span><span class="sxs-lookup"><span data-stu-id="7da00-180">Safety settings on this computer prohibit creation of business object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-181"><strong>IDS_RecordsetNotOpen</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-181"><strong>IDS_RecordsetNotOpen</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-182">4109</span><span class="sxs-lookup"><span data-stu-id="7da00-182">4109</span></span><br />
<span data-ttu-id="7da00-183">-2146824173</span><span class="sxs-lookup"><span data-stu-id="7da00-183">-2146824173</span></span><br />
<span data-ttu-id="7da00-184">0x800a1013</span><span class="sxs-lookup"><span data-stu-id="7da00-184">0x800A1013</span></span></p></td>
<td><p><span data-ttu-id="7da00-185">レコードセット (<strong>Recordset</strong>) が開かれていません。</span><span class="sxs-lookup"><span data-stu-id="7da00-185"><strong>Recordset</strong> is not open.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-186"><strong>IDS_ResetInvalidField</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-186"><strong>IDS_ResetInvalidField</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-187">4108</span><span class="sxs-lookup"><span data-stu-id="7da00-187">4108</span></span><br />
<span data-ttu-id="7da00-188">-2146824174</span><span class="sxs-lookup"><span data-stu-id="7da00-188">-2146824174</span></span><br />
<span data-ttu-id="7da00-189">0x800a1012</span><span class="sxs-lookup"><span data-stu-id="7da00-189">0x800A1012</span></span></p></td>
<td><p><span data-ttu-id="7da00-190"><strong>SortColumn</strong> または <strong>FilterColumn</strong> に指定された列は存在しません。</span><span class="sxs-lookup"><span data-stu-id="7da00-190">Column specified in <strong>SortColumn</strong> or <strong>FilterColumn</strong> does not exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-191"><strong>IDS_RowsetNotUpdateable</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-191"><strong>IDS_RowsetNotUpdateable</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-192">4104</span><span class="sxs-lookup"><span data-stu-id="7da00-192">4104</span></span><br />
<span data-ttu-id="7da00-193">-2146824184</span><span class="sxs-lookup"><span data-stu-id="7da00-193">-2146824184</span></span><br />
<span data-ttu-id="7da00-194">0x800a1008</span><span class="sxs-lookup"><span data-stu-id="7da00-194">0x800A1008</span></span></p></td>
<td><p><span data-ttu-id="7da00-195">行セットは更新できません。</span><span class="sxs-lookup"><span data-stu-id="7da00-195">Rowset not updateable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-196"><strong>IDS_UnexpectedError</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-196"><strong>IDS_UnexpectedError</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-197">4351</span><span class="sxs-lookup"><span data-stu-id="7da00-197">4351</span></span><br />
<span data-ttu-id="7da00-198">-2146823937</span><span class="sxs-lookup"><span data-stu-id="7da00-198">-2146823937</span></span><br />
<span data-ttu-id="7da00-199">0x800a10ff</span><span class="sxs-lookup"><span data-stu-id="7da00-199">0x800A10FF</span></span></p></td>
<td><p><span data-ttu-id="7da00-200">予期しないエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="7da00-200">Unexpected error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da00-201"><strong>IDS_UpdatesFailed</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-201"><strong>IDS_UpdatesFailed</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-202">4098</span><span class="sxs-lookup"><span data-stu-id="7da00-202">4098</span></span><br />
<span data-ttu-id="7da00-203">-2146824190</span><span class="sxs-lookup"><span data-stu-id="7da00-203">-2146824190</span></span><br />
<span data-ttu-id="7da00-204">0x800a1002</span><span class="sxs-lookup"><span data-stu-id="7da00-204">0x800A1002</span></span></p></td>
<td><p><span data-ttu-id="7da00-205">データベースを更新できません。</span><span class="sxs-lookup"><span data-stu-id="7da00-205">Unable to update database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da00-206"><strong>IDS_URLMONNotFound</strong></span><span class="sxs-lookup"><span data-stu-id="7da00-206"><strong>IDS_URLMONNotFound</strong></span></span></p></td>
<td><p><span data-ttu-id="7da00-207">4119</span><span class="sxs-lookup"><span data-stu-id="7da00-207">4119</span></span><br />
<span data-ttu-id="7da00-208">-2146824169</span><span class="sxs-lookup"><span data-stu-id="7da00-208">-2146824169</span></span><br />
<span data-ttu-id="7da00-209">0x800a1017</span><span class="sxs-lookup"><span data-stu-id="7da00-209">0x800A1017</span></span></p></td>
<td><p><span data-ttu-id="7da00-210">DataControl <strong>URL</strong> プロパティにはシステム ファイル Urlmon.dll が必要ですが、ファイルが見つかりません。</span><span class="sxs-lookup"><span data-stu-id="7da00-210">DataControl <strong>URL</strong> property requires the system file Urlmon.dll, which cannot be found.</span></span></p></td>
</tr>
</tbody>
</table>

