---
title: プロパティ. Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302900"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="e712b-102">プロパティ. Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="e712b-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="e712b-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="e712b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e712b-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e712b-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e712b-106">構文</span><span class="sxs-lookup"><span data-stu-id="e712b-106">Syntax</span></span>

<span data-ttu-id="e712b-107">*式*。種類</span><span class="sxs-lookup"><span data-stu-id="e712b-107">*expression* .Type</span></span>

<span data-ttu-id="e712b-108">\*式\***Property**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="e712b-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e712b-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e712b-109">Remarks</span></span>

<span data-ttu-id="e712b-p102">設定値または戻り値は、操作の種類またはデータ型を示す定数です。 **[Property](property-object-dao.md)** オブジェクトの場合、このプロパティは、オブジェクトがコレクションまたは他のオブジェクトに追加されるまでは値の取得と設定が可能で、追加後は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="e712b-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="e712b-112">**Property** オブジェクトで使用可能な設定値および戻り値を次の表に示します。</span><span class="sxs-lookup"><span data-stu-id="e712b-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e712b-113">定数</span><span class="sxs-lookup"><span data-stu-id="e712b-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="e712b-114">説明</span><span class="sxs-lookup"><span data-stu-id="e712b-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e712b-115"><strong>dbbigint</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-116">多倍長整数型 (Big Integer)</span><span class="sxs-lookup"><span data-stu-id="e712b-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-117"><strong>dbbinary</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-118">バイナリ型 (Binary)</span><span class="sxs-lookup"><span data-stu-id="e712b-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-119"><strong>dbboolean</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-120">ブール型 (Boolean)</span><span class="sxs-lookup"><span data-stu-id="e712b-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-121"><strong>dbbyte</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-122">バイト型 (Byte)</span><span class="sxs-lookup"><span data-stu-id="e712b-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-124">文字型 (Char)</span><span class="sxs-lookup"><span data-stu-id="e712b-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-125"><strong>dbcurrency</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-126">通貨型 (Currency)</span><span class="sxs-lookup"><span data-stu-id="e712b-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-127"><strong>dbdate</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-128">日付/時刻型 (Date/Time)</span><span class="sxs-lookup"><span data-stu-id="e712b-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-129"><strong>dbdecimal</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-130">10 進型 (Decimal)</span><span class="sxs-lookup"><span data-stu-id="e712b-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-131"><strong>dbdouble</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-132">倍精度浮動小数点型 (Double)</span><span class="sxs-lookup"><span data-stu-id="e712b-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-133"><strong>dbfloat</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-134">浮動小数点型 (Float)</span><span class="sxs-lookup"><span data-stu-id="e712b-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-135"><strong>dbguid</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-136">GUID 型 (GUID)</span><span class="sxs-lookup"><span data-stu-id="e712b-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-138">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="e712b-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-139"><strong>dblong</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-140">Long 型 (Long)</span><span class="sxs-lookup"><span data-stu-id="e712b-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-142">ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)</span><span class="sxs-lookup"><span data-stu-id="e712b-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-143"><strong>dbmemo</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-144">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="e712b-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-145"><strong>dbnumeric</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-146">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="e712b-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-147"><strong>dbsingle</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-148">単精度浮動小数点型 (Single)</span><span class="sxs-lookup"><span data-stu-id="e712b-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-149"><strong>dbtext</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-150">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="e712b-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-152">時刻型 (Time)</span><span class="sxs-lookup"><span data-stu-id="e712b-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e712b-153"><strong>dbtimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-154">タイムスタンプ型 (TimeStamp)</span><span class="sxs-lookup"><span data-stu-id="e712b-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e712b-155"><strong>dbvarbinary</strong></span><span class="sxs-lookup"><span data-stu-id="e712b-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="e712b-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="e712b-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e712b-157">新しい **Field** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e712b-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

