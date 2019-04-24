---
title: commandtypeenum (Access デスクトップデータベースリファレンス)
TOCTitle: CommandTypeEnum
ms:assetid: 9ad8f155-88a0-00eb-2855-1e1a2a677437
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249700(v=office.15)
ms:contentKeyID: 48546549
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a9114128771d4753265208dada763ac0c9f796d1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296116"
---
# <a name="commandtypeenum"></a><span data-ttu-id="637c6-102">CommandTypeEnum</span><span class="sxs-lookup"><span data-stu-id="637c6-102">CommandTypeEnum</span></span>

<span data-ttu-id="637c6-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="637c6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="637c6-104">コマンド引数の解釈方法を表します。</span><span class="sxs-lookup"><span data-stu-id="637c6-104">Specifies how a command argument should be interpreted.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="637c6-105">定数</span><span class="sxs-lookup"><span data-stu-id="637c6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="637c6-106">値</span><span class="sxs-lookup"><span data-stu-id="637c6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="637c6-107">説明</span><span class="sxs-lookup"><span data-stu-id="637c6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="637c6-108"><strong>adcmdunspecified</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-108"><strong>adCmdUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-109">-1</span><span class="sxs-lookup"><span data-stu-id="637c6-109">-1</span></span></p></td>
<td><p><span data-ttu-id="637c6-110">コマンドの種類の引数を指定しません。</span><span class="sxs-lookup"><span data-stu-id="637c6-110">Does not specify the command type argument.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="637c6-111"><strong>adcmdtext で</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-111"><strong>adCmdText</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-112">1-d</span><span class="sxs-lookup"><span data-stu-id="637c6-112">1</span></span></p></td>
<td><p><span data-ttu-id="637c6-113"><a href="commandtext-property-ado.md">CommandText</a> を、コマンドまたはストアド プロシージャのテキスト定義として評価します。</span><span class="sxs-lookup"><span data-stu-id="637c6-113">Evaluates <a href="commandtext-property-ado.md">CommandText</a> as a textual definition of a command or stored procedure call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="637c6-114"><strong>adcmdtable</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-114"><strong>adCmdTable</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-115">pbm-2</span><span class="sxs-lookup"><span data-stu-id="637c6-115">2</span></span></p></td>
<td><p><span data-ttu-id="637c6-116"><strong>CommandText</strong> を、内部的に生成された SQL クエリから返された列のみで構成されるテーブル名として評価します。</span><span class="sxs-lookup"><span data-stu-id="637c6-116">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned by an internally generated SQL query.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="637c6-117"><strong>adCmdStoredProc</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-117"><strong>adCmdStoredProc</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-118">2/4</span><span class="sxs-lookup"><span data-stu-id="637c6-118">4</span></span></p></td>
<td><p><span data-ttu-id="637c6-119"><strong>CommandText</strong> をストアド プロシージャ名として評価します。</span><span class="sxs-lookup"><span data-stu-id="637c6-119">Evaluates <strong>CommandText</strong> as a stored procedure name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="637c6-120"><strong>adcmdunknown</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-120"><strong>adCmdUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-121">~</span><span class="sxs-lookup"><span data-stu-id="637c6-121">8</span></span></p></td>
<td><p><span data-ttu-id="637c6-p101">既定値。<strong>CommandText</strong> プロパティのコマンドの種類が不明であることを示します。</span><span class="sxs-lookup"><span data-stu-id="637c6-p101">Default. Indicates that the type of command in the <strong>CommandText</strong> property is not known.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="637c6-124"><strong>adCmdFile</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-124"><strong>adCmdFile</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-125">256</span><span class="sxs-lookup"><span data-stu-id="637c6-125">256</span></span></p></td>
<td><p><span data-ttu-id="637c6-p102"><strong>CommandText</strong> を、保存された <a href="recordset-object-ado.md">Recordset</a> のファイル名として評価します。<strong>Recordset</strong>.<a href="open-method-ado-recordset.md">Open</a> または <a href="requery-method-ado.md">Requery</a> と組み合わせてのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="637c6-p102">Evaluates <strong>CommandText</strong> as the file name of a persistently stored <a href="recordset-object-ado.md">Recordset</a>. Used with <strong>Recordset.</strong><a href="open-method-ado-recordset.md">Open</a> or <a href="requery-method-ado.md">Requery</a> only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="637c6-128"><strong>adCmdTableDirect</strong></span><span class="sxs-lookup"><span data-stu-id="637c6-128"><strong>adCmdTableDirect</strong></span></span></p></td>
<td><p><span data-ttu-id="637c6-129">512</span><span class="sxs-lookup"><span data-stu-id="637c6-129">512</span></span></p></td>
<td><p><span data-ttu-id="637c6-130"><strong>CommandText</strong> を、すべての列が返されたテーブル名として評価します。</span><span class="sxs-lookup"><span data-stu-id="637c6-130">Evaluates <strong>CommandText</strong> as a table name whose columns are all returned.</span></span> <span data-ttu-id="637c6-131"><strong>Recordset.Open</strong> または <strong>Requery</strong> と組み合わせてのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="637c6-131">Used with <strong>Recordset.Open</strong> or <strong>Requery</strong> only.</span></span> <span data-ttu-id="637c6-132"><a href="seek-method-ado.md">Seek</a> メソッドを使用する場合、<strong>Recordset</strong> は <strong>adCmdTableDirect</strong> を指定して開く必要があります。</span><span class="sxs-lookup"><span data-stu-id="637c6-132">To use the <a href="seek-method-ado.md">Seek</a> method, the <strong>Recordset</strong> must be opened with <strong>adCmdTableDirect</strong>.</span></span> <span data-ttu-id="637c6-133">この値は、<a href="executeoptionenum.md">ExecuteOptionEnum</a> の値 <strong>adAsyncExecute</strong> と組み合わせて使用できません。</span><span class="sxs-lookup"><span data-stu-id="637c6-133">This value cannot be combined with the <a href="executeoptionenum.md">ExecuteOptionEnum</a> value <strong>adAsyncExecute</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="637c6-134">ADO/WFC と同等</span><span class="sxs-lookup"><span data-stu-id="637c6-134">ADO/WFC equivalent</span></span>

<span data-ttu-id="637c6-135">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="637c6-135">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="637c6-136">定数</span><span class="sxs-lookup"><span data-stu-id="637c6-136">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="637c6-137">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="637c6-137">AdoEnums.CommandType.UNSPECIFIED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="637c6-138">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="637c6-138">AdoEnums.CommandType.TEXT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="637c6-139">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="637c6-139">AdoEnums.CommandType.TABLE</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="637c6-140">AdoEnums STOREDPROC</span><span class="sxs-lookup"><span data-stu-id="637c6-140">AdoEnums.CommandType.STOREDPROC</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="637c6-141">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="637c6-141">AdoEnums.CommandType.UNKNOWN</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="637c6-142">AdoEnums</span><span class="sxs-lookup"><span data-stu-id="637c6-142">AdoEnums.CommandType.FILE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="637c6-143">AdoEnums 直接</span><span class="sxs-lookup"><span data-stu-id="637c6-143">AdoEnums.CommandType.TABLEDIRECT</span></span></p></td>
</tr>
</tbody>
</table>

