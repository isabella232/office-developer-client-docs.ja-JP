---
title: Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300946"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="44251-102">Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="44251-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="44251-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="44251-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="44251-p101">オブジェクトの操作の種類またはデータ型を示す値を設定あるいは取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="44251-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="44251-106">構文</span><span class="sxs-lookup"><span data-stu-id="44251-106">Syntax</span></span>

<span data-ttu-id="44251-107">*式*。種類</span><span class="sxs-lookup"><span data-stu-id="44251-107">*expression* .Type</span></span>

<span data-ttu-id="44251-108">\*式\***QueryDef**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="44251-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="44251-109">注釈</span><span class="sxs-lookup"><span data-stu-id="44251-109">Remarks</span></span>

<span data-ttu-id="44251-110">次の表は、**QueryDef** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="44251-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="44251-111">定数</span><span class="sxs-lookup"><span data-stu-id="44251-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="44251-112">クエリの種類</span><span class="sxs-lookup"><span data-stu-id="44251-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44251-113"><strong>dbqaction</strong></span><span class="sxs-lookup"><span data-stu-id="44251-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-114">アクション</span><span class="sxs-lookup"><span data-stu-id="44251-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44251-115"><strong>dbqappend</strong></span><span class="sxs-lookup"><span data-stu-id="44251-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-116">追加</span><span class="sxs-lookup"><span data-stu-id="44251-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44251-117"><strong>dbqcompound</strong></span><span class="sxs-lookup"><span data-stu-id="44251-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-118">複雑化</span><span class="sxs-lookup"><span data-stu-id="44251-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44251-119"><strong>dbqcrosstab 集計</strong></span><span class="sxs-lookup"><span data-stu-id="44251-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-120">行列</span><span class="sxs-lookup"><span data-stu-id="44251-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44251-121"><strong>dbqddl</strong></span><span class="sxs-lookup"><span data-stu-id="44251-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-122">データ定義</span><span class="sxs-lookup"><span data-stu-id="44251-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44251-123"><strong>dbqdelete</strong></span><span class="sxs-lookup"><span data-stu-id="44251-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-124">削除</span><span class="sxs-lookup"><span data-stu-id="44251-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44251-125"><strong>dbqmaketable</strong></span><span class="sxs-lookup"><span data-stu-id="44251-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-126">テーブル作成</span><span class="sxs-lookup"><span data-stu-id="44251-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44251-127"><strong>dbqprocedure</strong></span><span class="sxs-lookup"><span data-stu-id="44251-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-128">プロシージャ (ODBCDirect ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="44251-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="44251-129"><strong>注</strong>: ODBCDirect ワークスペースは、Microsoft access 2013 ではサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="44251-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="44251-130">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="44251-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44251-131"><strong>dbqselect</strong></span><span class="sxs-lookup"><span data-stu-id="44251-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-132">Select</span><span class="sxs-lookup"><span data-stu-id="44251-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44251-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="44251-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-134">Union</span><span class="sxs-lookup"><span data-stu-id="44251-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44251-135"><strong>dbqsptbulk</strong></span><span class="sxs-lookup"><span data-stu-id="44251-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-136"><strong>dbQSQLPassThrough</strong> と共に使用して、レコードを取得しないクエリを指定 (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="44251-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44251-137"><strong>dbqsqlpassthrough</strong></span><span class="sxs-lookup"><span data-stu-id="44251-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-138">パススルー (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="44251-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44251-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="44251-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="44251-140">Update</span><span class="sxs-lookup"><span data-stu-id="44251-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="44251-141">新しい **[Field](field-object-dao.md)** オブジェクト、 **[Parameter](parameter-object-dao.md)** オブジェクト、または **[Property](property-object-dao.md)** オブジェクトを、 **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **[Recordset](recordset-object-dao.md)** オブジェクト、または **[TableDef](tabledef-object-dao.md)** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="44251-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

