---
title: Field.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c8f212c5e1f10f4270987c9453802575d88cebfa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292952"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="75919-102">Field.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="75919-102">Field.Type Property (DAO)</span></span>


<span data-ttu-id="75919-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="75919-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="75919-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 (**Integer**) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="75919-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="75919-106">構文</span><span class="sxs-lookup"><span data-stu-id="75919-106">Syntax</span></span>

<span data-ttu-id="75919-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="75919-107">expression  . Type</span></span>

<span data-ttu-id="75919-108">*expression*: **Field** オブジェクトを表す変数。</span><span class="sxs-lookup"><span data-stu-id="75919-108">*expression*  A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="75919-109">注釈</span><span class="sxs-lookup"><span data-stu-id="75919-109">Remarks</span></span>

<span data-ttu-id="75919-p102">設定値または戻り値は、操作の種類またはデータ型を示す定数です。 **Field** オブジェクトの場合、このプロパティは、オブジェクトがコレクションまたは他のオブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="75919-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="75919-112">次の表は、 **Field** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="75919-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="75919-113">定数</span><span class="sxs-lookup"><span data-stu-id="75919-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="75919-114">説明</span><span class="sxs-lookup"><span data-stu-id="75919-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="75919-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="75919-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-116">多倍長整数型 (Big Integer)</span><span class="sxs-lookup"><span data-stu-id="75919-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="75919-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-118">Binary</span><span class="sxs-lookup"><span data-stu-id="75919-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="75919-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-120">Boolean</span><span class="sxs-lookup"><span data-stu-id="75919-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="75919-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-122">バイト型 (Byte)</span><span class="sxs-lookup"><span data-stu-id="75919-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="75919-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-124">Char</span><span class="sxs-lookup"><span data-stu-id="75919-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="75919-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-126">通貨</span><span class="sxs-lookup"><span data-stu-id="75919-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="75919-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-128">日付/時刻</span><span class="sxs-lookup"><span data-stu-id="75919-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="75919-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="75919-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="75919-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-132">2 行分</span><span class="sxs-lookup"><span data-stu-id="75919-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="75919-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-134">浮動小数点数</span><span class="sxs-lookup"><span data-stu-id="75919-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="75919-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-136">GUID</span><span class="sxs-lookup"><span data-stu-id="75919-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="75919-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-138">整数</span><span class="sxs-lookup"><span data-stu-id="75919-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="75919-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-140">Long</span><span class="sxs-lookup"><span data-stu-id="75919-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="75919-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-142">ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)</span><span class="sxs-lookup"><span data-stu-id="75919-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="75919-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-144">メモ</span><span class="sxs-lookup"><span data-stu-id="75919-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="75919-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-146">数値</span><span class="sxs-lookup"><span data-stu-id="75919-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="75919-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-148">1 行</span><span class="sxs-lookup"><span data-stu-id="75919-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="75919-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-150">テキスト</span><span class="sxs-lookup"><span data-stu-id="75919-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="75919-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-152">Time</span><span class="sxs-lookup"><span data-stu-id="75919-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="75919-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="75919-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-154">タイム スタンプ</span><span class="sxs-lookup"><span data-stu-id="75919-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="75919-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="75919-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="75919-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="75919-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="75919-157">新しい **Field** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="75919-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

