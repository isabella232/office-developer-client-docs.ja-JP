---
title: CommandTypeEnum (デスクトップ データベース参照のアクセス)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: cc5fee66746270f5ba8ee851010c6860cfc9e791
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861065"
---
# <a name="commandtypeenum"></a><span data-ttu-id="8412a-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="8412a-102">CommandTypeEnum</span></span>

<span data-ttu-id="8412a-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="8412a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8412a-104">コマンド引数の解釈方法を表します。</span><span class="sxs-lookup"><span data-stu-id="8412a-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8412a-105">定数</span><span class="sxs-lookup"><span data-stu-id="8412a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="8412a-106">値</span><span class="sxs-lookup"><span data-stu-id="8412a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="8412a-107">説明</span><span class="sxs-lookup"><span data-stu-id="8412a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8412a-108"><strong>adCmdUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-109">-1</span><span class="sxs-lookup"><span data-stu-id="8412a-109">-1</span></span></p></td>
<td><p><span data-ttu-id="8412a-110">コマンドの種類の引数を指定しません。</span><span class="sxs-lookup"><span data-stu-id="8412a-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-111"><strong>adCmdText</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-112">1</span><span class="sxs-lookup"><span data-stu-id="8412a-112">1</span></span></p></td>
<td><p><span data-ttu-id="8412a-113"><a href="commandtext-property-ado.md">CommandText</a> を、コマンドまたはストアド プロシージャのテキスト定義として評価します。</span><span class="sxs-lookup"><span data-stu-id="8412a-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-114"><strong>adCmdTable</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-115">2</span><span class="sxs-lookup"><span data-stu-id="8412a-115">2</span></span></p></td>
<td><p><span data-ttu-id="8412a-116"><strong>CommandText</strong> を、内部的に生成された SQL クエリから返された列のみで構成されるテーブル名として評価します。</span><span class="sxs-lookup"><span data-stu-id="8412a-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-118">4</span><span class="sxs-lookup"><span data-stu-id="8412a-118">4</span></span></p></td>
<td><p><span data-ttu-id="8412a-119"><strong>CommandText</strong> をストアド プロシージャ名として評価します。</span><span class="sxs-lookup"><span data-stu-id="8412a-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-120"><strong>adCmdUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-121">8</span><span class="sxs-lookup"><span data-stu-id="8412a-121">8</span></span></p></td>
<td><p><span data-ttu-id="8412a-p101">既定値。<strong>CommandText</strong> プロパティのコマンドの種類が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="8412a-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-125">256</span><span class="sxs-lookup"><span data-stu-id="8412a-125">256</span></span></p></td>
<td><p><span data-ttu-id="8412a-p102"><strong>CommandText</strong> を、保存された <a href="recordset-object-ado.md">Recordset</a> のファイル名として評価します。<strong>Recordset</strong>.<a href="open-method-ado-recordset.md">Open</a> または <a href="requery-method-ado.md">Requery</a> と組み合わせてのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="8412a-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="8412a-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="8412a-129">512</span><span class="sxs-lookup"><span data-stu-id="8412a-129">512</span></span></p></td>
<td><p><span data-ttu-id="8412a-130"><strong>CommandText</strong>を指定された列は、返されたすべてのテーブル名として評価します。</span><span class="sxs-lookup"><span data-stu-id="8412a-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="8412a-131"><strong>Recordset.Open</strong>または<strong>Requery</strong>とのみに使用します。</span><span class="sxs-lookup"><span data-stu-id="8412a-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="8412a-132"><a href="seek-method-ado.md">Seek</a>メソッドを使用するには、 <strong>adCmdTableDirect</strong>に<strong>レコード セット</strong>を開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="8412a-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="8412a-133">この値は、<a href="executeoptionenum.md">ExecuteOptionEnum</a> の値 <strong>adAsyncExecute</strong> と組み合わせて使用できません。</span><span class="sxs-lookup"><span data-stu-id="8412a-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="8412a-134">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="8412a-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="8412a-135">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="8412a-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8412a-136">定数</span><span class="sxs-lookup"><span data-stu-id="8412a-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8412a-137">AdoEnums.CommandType.UNSPECIFIED</span><span class="sxs-lookup"><span data-stu-id="8412a-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-138">AdoEnums.CommandType.TEXT</span><span class="sxs-lookup"><span data-stu-id="8412a-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-139">AdoEnums.CommandType.TABLE</span><span class="sxs-lookup"><span data-stu-id="8412a-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-140">AdoEnums.CommandType.STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="8412a-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-141">AdoEnums.CommandType.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="8412a-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8412a-142">AdoEnums.CommandType.FILE</span><span class="sxs-lookup"><span data-stu-id="8412a-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8412a-143">AdoEnums.CommandType.TABLEDIRECT</span><span class="sxs-lookup"><span data-stu-id="8412a-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

