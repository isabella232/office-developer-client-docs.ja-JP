---
title: Field2 プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4da32f18a2b3e9dddbb0ae04e3257de34ba09761
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292665"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="adb19-102">Field2 プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="adb19-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="adb19-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="adb19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="adb19-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="adb19-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="adb19-106">構文</span><span class="sxs-lookup"><span data-stu-id="adb19-106">Syntax</span></span>

<span data-ttu-id="adb19-107">*式*。種類</span><span class="sxs-lookup"><span data-stu-id="adb19-107">*expression* .Type</span></span>

<span data-ttu-id="adb19-108">\*式\***Field2**オブジェクトを表す変数を取得します。</span><span class="sxs-lookup"><span data-stu-id="adb19-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="adb19-109">注釈</span><span class="sxs-lookup"><span data-stu-id="adb19-109">Remarks</span></span>

<span data-ttu-id="adb19-p102">設定値または戻り値は、操作の種類またはデータ型を示す定数です。 **Field2** オブジェクトの場合、このプロパティは、オブジェクトがコレクションまたは他のオブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="adb19-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="adb19-112">次の表は、 **Field2** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="adb19-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="adb19-113">定数</span><span class="sxs-lookup"><span data-stu-id="adb19-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="adb19-114">説明</span><span class="sxs-lookup"><span data-stu-id="adb19-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adb19-115"><strong>dbbigint</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-116">多倍長整数型 (Big Integer)</span><span class="sxs-lookup"><span data-stu-id="adb19-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-117"><strong>dbbinary</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-118">バイナリ型 (Binary)</span><span class="sxs-lookup"><span data-stu-id="adb19-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-119"><strong>dbboolean</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-120">ブール型 (Boolean)</span><span class="sxs-lookup"><span data-stu-id="adb19-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-121"><strong>dbbyte</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-122">バイト型 (Byte)</span><span class="sxs-lookup"><span data-stu-id="adb19-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-124">文字型 (Char)</span><span class="sxs-lookup"><span data-stu-id="adb19-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-125"><strong>dbcurrency</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-126">通貨型 (Currency)</span><span class="sxs-lookup"><span data-stu-id="adb19-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-127"><strong>dbdate</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-128">日付/時刻型 (Date/Time)</span><span class="sxs-lookup"><span data-stu-id="adb19-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-129"><strong>dbdecimal</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-130">10 進型 (Decimal)</span><span class="sxs-lookup"><span data-stu-id="adb19-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-131"><strong>dbdouble</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-132">倍精度浮動小数点型 (Double)</span><span class="sxs-lookup"><span data-stu-id="adb19-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-133"><strong>dbfloat</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-134">浮動小数点型 (Float)</span><span class="sxs-lookup"><span data-stu-id="adb19-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-135"><strong>dbguid</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-136">GUID 型 (GUID)</span><span class="sxs-lookup"><span data-stu-id="adb19-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-138">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="adb19-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-139"><strong>dblong</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-140">Long 型 (Long)</span><span class="sxs-lookup"><span data-stu-id="adb19-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-142">ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)</span><span class="sxs-lookup"><span data-stu-id="adb19-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-143"><strong>dbmemo</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-144">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="adb19-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-145"><strong>dbnumeric</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-146">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="adb19-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-147"><strong>dbsingle</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-148">単精度浮動小数点型 (Single)</span><span class="sxs-lookup"><span data-stu-id="adb19-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-149"><strong>dbtext</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-150">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="adb19-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-152">時刻型 (Time)</span><span class="sxs-lookup"><span data-stu-id="adb19-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adb19-153"><strong>dbtimestamp</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-154">タイムスタンプ型 (TimeStamp)</span><span class="sxs-lookup"><span data-stu-id="adb19-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adb19-155"><strong>dbvarbinary</strong></span><span class="sxs-lookup"><span data-stu-id="adb19-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="adb19-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="adb19-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="adb19-157">新しい **Field2** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **Index** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="adb19-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

