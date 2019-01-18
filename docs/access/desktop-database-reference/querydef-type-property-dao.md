---
title: QueryDef.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: cb8856194d0b2ed14577bdc275adeb50ebdde212
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721382"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="0de79-102">QueryDef.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="0de79-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="0de79-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="0de79-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0de79-p101">オブジェクトの操作の種類またはデータ型を示す値を設定あるいは取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0de79-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="0de79-106">構文</span><span class="sxs-lookup"><span data-stu-id="0de79-106">Syntax</span></span>

<span data-ttu-id="0de79-107">*式*です。タイプ</span><span class="sxs-lookup"><span data-stu-id="0de79-107">*expression* .Type</span></span>

<span data-ttu-id="0de79-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="0de79-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="0de79-109">注釈</span><span class="sxs-lookup"><span data-stu-id="0de79-109">Remarks</span></span>

<span data-ttu-id="0de79-110">次の表は、 **QueryDef** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="0de79-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0de79-111">定数</span><span class="sxs-lookup"><span data-stu-id="0de79-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="0de79-112">クエリの種類</span><span class="sxs-lookup"><span data-stu-id="0de79-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0de79-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-114">Action</span><span class="sxs-lookup"><span data-stu-id="0de79-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de79-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-116">追加</span><span class="sxs-lookup"><span data-stu-id="0de79-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de79-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-118">複合</span><span class="sxs-lookup"><span data-stu-id="0de79-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de79-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-120">クロス集計</span><span class="sxs-lookup"><span data-stu-id="0de79-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de79-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-122">データ定義</span><span class="sxs-lookup"><span data-stu-id="0de79-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de79-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-124">Delete</span><span class="sxs-lookup"><span data-stu-id="0de79-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de79-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-126">テーブル作成</span><span class="sxs-lookup"><span data-stu-id="0de79-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de79-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-128">プロシージャ (ODBCDirect ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="0de79-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="0de79-129"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="0de79-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0de79-130">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="0de79-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de79-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-132">選択</span><span class="sxs-lookup"><span data-stu-id="0de79-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de79-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-134">ユニオン</span><span class="sxs-lookup"><span data-stu-id="0de79-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de79-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-136"><strong>dbQSQLPassThrough</strong> と共に使用して、レコードを取得しないクエリを指定 (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="0de79-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0de79-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-138">パススルー (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="0de79-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0de79-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="0de79-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="0de79-140">Update</span><span class="sxs-lookup"><span data-stu-id="0de79-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0de79-141">新しい **[Field](field-object-dao.md)** オブジェクト、 **[Parameter](parameter-object-dao.md)** オブジェクト、または **[Property](property-object-dao.md)** オブジェクトを、 **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **[Recordset](recordset-object-dao.md)** オブジェクト、または **[TableDef](tabledef-object-dao.md)** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="0de79-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

