---
title: QueryDef.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bd958c4b2123c727c3bc0a14a067fcb719ec86b3
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026387"
---
# <a name="querydeftype-property-dao"></a><span data-ttu-id="2767a-102">QueryDef.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="2767a-102">QueryDef.Type property (DAO)</span></span>


<span data-ttu-id="2767a-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2767a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2767a-p101">オブジェクトの操作の種類またはデータ型を示す値を設定あるいは取得します。値の取得のみ可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2767a-p101">Sets or returns a value that indicates the operational type or data type of an object. Read-only**Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="2767a-106">構文</span><span class="sxs-lookup"><span data-stu-id="2767a-106">Syntax</span></span>

<span data-ttu-id="2767a-107">*式*です。タイプ</span><span class="sxs-lookup"><span data-stu-id="2767a-107">*expression* .Type</span></span>

<span data-ttu-id="2767a-108">\*式\***クエリ定義**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="2767a-108">*expression* A variable that represents a **QueryDef** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2767a-109">注釈</span><span class="sxs-lookup"><span data-stu-id="2767a-109">Remarks</span></span>

<span data-ttu-id="2767a-110">次の表は、 **QueryDef** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="2767a-110">For a **QueryDef** object, the possible settings and return values are shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2767a-111">定数</span><span class="sxs-lookup"><span data-stu-id="2767a-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="2767a-112">クエリの種類</span><span class="sxs-lookup"><span data-stu-id="2767a-112">Query type</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2767a-113"><strong>dbQAction</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-113"><strong>dbQAction</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-114">アクション</span><span class="sxs-lookup"><span data-stu-id="2767a-114">Action</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2767a-115"><strong>dbQAppend</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-115"><strong>dbQAppend</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-116">追加</span><span class="sxs-lookup"><span data-stu-id="2767a-116">Append</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2767a-117"><strong>dbQCompound</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-117"><strong>dbQCompound</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-118">複合</span><span class="sxs-lookup"><span data-stu-id="2767a-118">Compound</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2767a-119"><strong>dbQCrosstab</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-119"><strong>dbQCrosstab</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-120">クロス集計</span><span class="sxs-lookup"><span data-stu-id="2767a-120">Crosstab</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2767a-121"><strong>dbQDDL</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-121"><strong>dbQDDL</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-122">データ定義</span><span class="sxs-lookup"><span data-stu-id="2767a-122">Data-definition</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2767a-123"><strong>dbQDelete</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-123"><strong>dbQDelete</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-124">削除</span><span class="sxs-lookup"><span data-stu-id="2767a-124">Delete</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2767a-125"><strong>dbQMakeTable</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-125"><strong>dbQMakeTable</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-126">テーブル作成</span><span class="sxs-lookup"><span data-stu-id="2767a-126">Make-table</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2767a-127"><strong>dbQProcedure</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-127"><strong>dbQProcedure</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-128">プロシージャ (ODBCDirect ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="2767a-128">Procedure (ODBCDirect workspaces only)</span></span></p><p><span data-ttu-id="2767a-129"><strong>注</strong>: Microsoft Access 2013 では、ODBCDirect ワークスペースはサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="2767a-129"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2767a-130">Microsoft Access データベース エンジンを使用しないで外部データ ソースにアクセスする場合は、ADO を使用してください。</span><span class="sxs-lookup"><span data-stu-id="2767a-130">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2767a-131"><strong>dbQSelect</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-131"><strong>dbQSelect</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-132">選択</span><span class="sxs-lookup"><span data-stu-id="2767a-132">Select</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2767a-133"><strong>dbQSetOperation</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-133"><strong>dbQSetOperation</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-134">ユニオン</span><span class="sxs-lookup"><span data-stu-id="2767a-134">Union</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2767a-135"><strong>dbQSPTBulk</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-135"><strong>dbQSPTBulk</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-136"><strong>dbQSQLPassThrough</strong> と共に使用して、レコードを取得しないクエリを指定 (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="2767a-136">Used with <strong>dbQSQLPassThrough</strong> to specify a query that doesn't return records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2767a-137"><strong>dbQSQLPassThrough</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-137"><strong>dbQSQLPassThrough</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-138">パススルー (Microsoft Access ワークスペースのみ)</span><span class="sxs-lookup"><span data-stu-id="2767a-138">Pass-through (Microsoft Access workspaces only)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2767a-139"><strong>dbQUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="2767a-139"><strong>dbQUpdate</strong></span></span></p></td>
<td><p><span data-ttu-id="2767a-140">Update</span><span class="sxs-lookup"><span data-stu-id="2767a-140">Update</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2767a-141">新しい **[Field](field-object-dao.md)** オブジェクト、 **[Parameter](parameter-object-dao.md)** オブジェクト、または **[Property](property-object-dao.md)** オブジェクトを、 **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **[Recordset](recordset-object-dao.md)** オブジェクト、または **[TableDef](tabledef-object-dao.md)** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2767a-141">When you append a new **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)**, or **[Property](property-object-dao.md)** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)**, or **[TableDef](tabledef-object-dao.md)** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

