---
title: executeoptionenum (Access デスクトップデータベースリファレンス)
TOCTitle: ExecuteOptionEnum
ms:assetid: bd6d44a3-e471-7aa0-3e65-6775334de2ff
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249915(v=office.15)
ms:contentKeyID: 48547438
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: febeb3b52eb579647c995b01d6723a5c1f1b0c1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293246"
---
# <a name="executeoptionenum"></a><span data-ttu-id="348dd-102">ExecuteOptionEnum</span><span class="sxs-lookup"><span data-stu-id="348dd-102">ExecuteOptionEnum</span></span>

<span data-ttu-id="348dd-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="348dd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="348dd-104">プロバイダーによるコマンドの実行方法を表します。</span><span class="sxs-lookup"><span data-stu-id="348dd-104">Specifies how a provider should execute a command.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="348dd-105">定数</span><span class="sxs-lookup"><span data-stu-id="348dd-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="348dd-106">値</span><span class="sxs-lookup"><span data-stu-id="348dd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="348dd-107">説明</span><span class="sxs-lookup"><span data-stu-id="348dd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="348dd-108"><strong>adAsyncExecute</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-108"><strong>adAsyncExecute</strong></span></span></p></td>
<td><p><span data-ttu-id="348dd-109">0x10</span><span class="sxs-lookup"><span data-stu-id="348dd-109">0x10</span></span></p></td>
<td><p><span data-ttu-id="348dd-110">コマンドを非同期に実行することを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-110">Indicates that the command should execute asynchronously.</span></span> <span data-ttu-id="348dd-111">この値は、<a href="commandtypeenum.md">CommandTypeEnum</a> の値 <strong>adCmdTableDirect</strong> と組み合わせて使用できません。</span><span class="sxs-lookup"><span data-stu-id="348dd-111">This value cannot be combined with the <a href="commandtypeenum.md">CommandTypeEnum</a> value <strong>adCmdTableDirect</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="348dd-112"><strong>adAsyncFetch</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-112"><strong>adAsyncFetch</strong></span></span></p></td>
<td><p><span data-ttu-id="348dd-113">0x20</span><span class="sxs-lookup"><span data-stu-id="348dd-113">0x20</span></span></p></td>
<td><p><span data-ttu-id="348dd-114"><a href="cachesize-property-ado.md">CacheSize</a> プロパティで指定した初期量の残りの行を非同期に取得することを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-114">Indicates that the remaining rows after the initial quantity specified in the <a href="cachesize-property-ado.md">CacheSize</a> property should be retrieved asynchronously.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="348dd-115"><strong>adAsyncFetchNonBlocking</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-115"><strong>adAsyncFetchNonBlocking</strong></span></span></p></td>
<td><p><span data-ttu-id="348dd-116">0x40</span><span class="sxs-lookup"><span data-stu-id="348dd-116">0x40</span></span></p></td>
<td><p><span data-ttu-id="348dd-117">取得中にメイン スレッドがブロックしないことを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-117">Indicates that the main thread never blocks while retrieving.</span></span> <span data-ttu-id="348dd-118">要求された行がまだ取得されていない場合、現在の行が自動的にファイルの最後に移動します。</span><span class="sxs-lookup"><span data-stu-id="348dd-118">If the requested row has not been retrieved, the current row automatically moves to the end of the file.</span></span></p><p><span data-ttu-id="348dd-119">永続的に保存された <strong>Recordset</strong> を持つ <a href="stream-object-ado.md">Stream</a> から <a href="recordset-object-ado.md">Recordset</a> を開いた場合、<strong>adAsyncFetchNonBlocking</strong> は無効になり、操作は同期で実行され、ブロッキングが発生します。</span><span class="sxs-lookup"><span data-stu-id="348dd-119">If you open a <a href="recordset-object-ado.md">Recordset</a> from a <a href="stream-object-ado.md">Stream</a> containing a persistently stored <strong>Recordset</strong>, <strong>adAsyncFetchNonBlocking</strong> will not have an effect; the operation will be synchronous and blocking.</span></span> <span data-ttu-id="348dd-120"><a href="commandtypeenum.md">adCmdTableDirect</a> オプションを使用して <strong>Recordset</strong> を開いた場合、<strong>adAsynchFetchNonBlocking</strong> は無効になります。</span><span class="sxs-lookup"><span data-stu-id="348dd-120"><strong>adAsynchFetchNonBlocking</strong> has no effect when the <a href="commandtypeenum.md">adCmdTableDirect</a> option is used to open the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="348dd-121"><strong>adExecuteNoRecords</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-121"><strong>adExecuteNoRecords</strong></span></span></p></td>
<td><p><span data-ttu-id="348dd-122">0x80</span><span class="sxs-lookup"><span data-stu-id="348dd-122">0x80</span></span></p></td>
<td><p><span data-ttu-id="348dd-123">コマンド テキストが、行を返さないコマンドまたはストアド プロシージャ (たとえば、データの挿入のみを行うコマンド) であることを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-123">Indicates that the command text is a command or stored procedure that does not return rows (for example, a command that only inserts data).</span></span> <span data-ttu-id="348dd-124">取得した行があっても削除されるので、コマンドからは返されません。</span><span class="sxs-lookup"><span data-stu-id="348dd-124">If any rows are retrieved, they are discarded and not returned.</span></span> <span data-ttu-id="348dd-125"><strong>adExecuteNoRecords</strong>は、<strong>コマンド</strong>または<strong>Connection</strong>の<strong>Execute</strong>メソッドに、省略可能なパラメーターとしてのみ渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="348dd-125"><strong>adExecuteNoRecords</strong> can only be passed as an optional parameter to the <strong>Command</strong> or <strong>Connection</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="348dd-126"><strong>adExecuteStream</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-126"><strong>adExecuteStream</strong></span></span></p></td>
<td><p><span data-ttu-id="348dd-127">解像度</span><span class="sxs-lookup"><span data-stu-id="348dd-127">0x400</span></span></p></td>
<td><p><span data-ttu-id="348dd-128">コマンドの実行結果がストリームとして返されることを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-128">Indicates that the results of a command execution should be returned as a stream.</span></span> <span data-ttu-id="348dd-129"><strong>adExecuteStream</strong>は、 <strong>Command</strong> <strong>Execute</strong>メソッドにオプションのパラメーターとして渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="348dd-129"><strong>adExecuteStream</strong> can only be passed as an optional parameter to the <strong>Command</strong> <strong>Execute</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="348dd-130"><strong>adExecuteRecord</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-130"><strong>adExecuteRecord</strong></span></span></p></td>
<td><p><br />
</p></td>
<td><p><span data-ttu-id="348dd-131"><strong>CommandText</strong> が、<strong>Record</strong> オブジェクトとして返される単一の行を返すコマンドまたはストアド プロシージャであることを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-131">Indicates that the <strong>CommandText</strong> is a command or stored procedure that returns a single row which should be returned as a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="348dd-132"><strong>adoptionunspecified</strong></span><span class="sxs-lookup"><span data-stu-id="348dd-132"><strong>adOptionUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="348dd-133">-1</span><span class="sxs-lookup"><span data-stu-id="348dd-133">-1</span></span></p></td>
<td><p><span data-ttu-id="348dd-134">コマンドが指定されていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="348dd-134">Indicates that the command is unspecified.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="348dd-135">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="348dd-135">ADO/WFC equivalent</span></span>

<span data-ttu-id="348dd-136">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="348dd-136">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="348dd-137">定数</span><span class="sxs-lookup"><span data-stu-id="348dd-137">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="348dd-138">AdoEnums オプションの asyncexecute</span><span class="sxs-lookup"><span data-stu-id="348dd-138">AdoEnums.ExecuteOption.ASYNCEXECUTE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="348dd-139">AdoEnums のオプション。 asyncfetch</span><span class="sxs-lookup"><span data-stu-id="348dd-139">AdoEnums.ExecuteOption.ASYNCFETCH</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="348dd-140">AdoEnums オプション。 asyncfetchnonblocking ブロッキング</span><span class="sxs-lookup"><span data-stu-id="348dd-140">AdoEnums.ExecuteOption.ASYNCFETCHNONBLOCKING</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="348dd-141">AdoEnums NORECORDS</span><span class="sxs-lookup"><span data-stu-id="348dd-141">AdoEnums.ExecuteOption.NORECORDS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="348dd-142">AdoEnums オプション。未指定</span><span class="sxs-lookup"><span data-stu-id="348dd-142">AdoEnums.ExecuteOption.UNSPECIFIED</span></span></p></td>
</tr>
</tbody>
</table>

