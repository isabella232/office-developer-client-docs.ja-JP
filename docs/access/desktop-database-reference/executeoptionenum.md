---
title: ExecuteOptionEnum (デスクトップ データベース参照のアクセス)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718309"
---
# <a name="executeoptionenum"></a><span data-ttu-id="cdd99-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="cdd99-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="cdd99-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="cdd99-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cdd99-104">プロバイダーによるコマンドの実行方法を表します。</span><span class="sxs-lookup"><span data-stu-id="cdd99-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdd99-105">定数</span><span class="sxs-lookup"><span data-stu-id="cdd99-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cdd99-106">値</span><span class="sxs-lookup"><span data-stu-id="cdd99-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cdd99-107">説明</span><span class="sxs-lookup"><span data-stu-id="cdd99-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd99-109">0x10</span><span class="sxs-lookup"><span data-stu-id="cdd99-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="cdd99-110">コマンドを非同期に実行することを示します。
</span><span class="sxs-lookup"><span data-stu-id="cdd99-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="cdd99-111">この値は、<a href="commandtypeenum.md">CommandTypeEnum</a> の値 <strong>adCmdTableDirect</strong> と組み合わせて使用できません。</span><span class="sxs-lookup"><span data-stu-id="cdd99-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd99-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd99-113">0x20</span><span class="sxs-lookup"><span data-stu-id="cdd99-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="cdd99-114"><a href="cachesize-property-ado.md">CacheSize</a> プロパティで指定した初期量の残りの行を非同期に取得することを示します。</span><span class="sxs-lookup"><span data-stu-id="cdd99-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd99-116">0x40</span><span class="sxs-lookup"><span data-stu-id="cdd99-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="cdd99-p102">取得中にメイン スレッドがブロックしないことを示します。要求された行がまだ取得されていない場合、現在の行が自動的にファイルの最後に移動します。
</span><span class="sxs-lookup"><span data-stu-id="cdd99-p102">Indicates that the main thread never blocks while retrieving. If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="cdd99-119">永続的に保存された <strong>Recordset</strong> を持つ <a href="stream-object-ado.md">Stream</a> から <a href="recordset-object-ado.md">Recordset</a> を開いた場合、<strong>adAsyncFetchNonBlocking</strong> は無効になり、操作は同期で実行され、ブロッキングが発生します。</span><span class="sxs-lookup"><span data-stu-id="cdd99-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="cdd99-120"><a href="commandtypeenum.md">adCmdTableDirect</a> オプションを使用して <strong>Recordset</strong> を開いた場合、<strong>adAsynchFetchNonBlocking</strong> は無効になります。</span><span class="sxs-lookup"><span data-stu-id="cdd99-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd99-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd99-122">0x80</span><span class="sxs-lookup"><span data-stu-id="cdd99-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="cdd99-123">コマンド テキストは、コマンドまたはストアド プロシージャ (たとえば、だけデータを挿入するコマンド) の行を返さないことを示します。</span><span class="sxs-lookup"><span data-stu-id="cdd99-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="cdd99-124">すべての行を取得する場合、破棄され、返されません。</span><span class="sxs-lookup"><span data-stu-id="cdd99-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="cdd99-125"><strong>adExecuteNoRecords</strong>は、<strong>コマンド</strong>または<strong>接続</strong>の<strong>Execute</strong>メソッドにオプションのパラメーターとしてだけ渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="cdd99-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd99-127">0x400</span><span class="sxs-lookup"><span data-stu-id="cdd99-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="cdd99-128">コマンドの実行結果がストリームとして返されることを示します。
</span><span class="sxs-lookup"><span data-stu-id="cdd99-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="cdd99-129"><strong>adExecuteStream</strong>は、<strong>コマンド</strong>の<strong>Execute</strong>メソッドにオプションのパラメーターとしてだけ渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="cdd99-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd99-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="cdd99-131"><strong>CommandText</strong> が、<strong>Record</strong> オブジェクトとして返される単一の行を返すコマンドまたはストアド プロシージャであることを示します。</span><span class="sxs-lookup"><span data-stu-id="cdd99-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-132"><strong>adOptionUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="cdd99-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="cdd99-133">-1</span><span class="sxs-lookup"><span data-stu-id="cdd99-133">-1</span></span></p></td>
<td><p><span data-ttu-id="cdd99-134">コマンドが指定されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="cdd99-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cdd99-135">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="cdd99-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="cdd99-136">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cdd99-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cdd99-137">定数</span><span class="sxs-lookup"><span data-stu-id="cdd99-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span><span class="sxs-lookup"><span data-stu-id="cdd99-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd99-139">AdoEnums.ExecuteOption.ASYNCFETCH</span><span class="sxs-lookup"><span data-stu-id="cdd99-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span><span class="sxs-lookup"><span data-stu-id="cdd99-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdd99-141">AdoEnums.ExecuteOption.NORECORDS</span><span class="sxs-lookup"><span data-stu-id="cdd99-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdd99-142">AdoEnums.ExecuteOption.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="cdd99-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

