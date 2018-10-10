---
title: Field.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: dab800e390e6ceaa6bf473e54d7d576f5e6023f4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479281"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="beeee-102">Field.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="beeee-102">Field.Type Property (DAO)</span></span>


<span data-ttu-id="beeee-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="beeee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="beeee-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 ( **Integer** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="beeee-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="beeee-106">構文</span><span class="sxs-lookup"><span data-stu-id="beeee-106">Syntax</span></span>

<span data-ttu-id="beeee-107">*式*です。タイプ</span><span class="sxs-lookup"><span data-stu-id="beeee-107">*expression* .Type</span></span>

<span data-ttu-id="beeee-108">\*式\***Field**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="beeee-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="beeee-109">解説</span><span class="sxs-lookup"><span data-stu-id="beeee-109">Remarks</span></span>

<span data-ttu-id="beeee-p102">設定値または戻り値は、操作の種類またはデータ型を示す定数です。 **Field** オブジェクトの場合、このプロパティは、オブジェクトがコレクションまたは他のオブジェクトに追加されるまでは値の設定と取得が可能で、追加後は値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="beeee-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="beeee-112">次の表は、 **Field** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="beeee-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="beeee-113">定数</span><span class="sxs-lookup"><span data-stu-id="beeee-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="beeee-114">説明</span><span class="sxs-lookup"><span data-stu-id="beeee-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="beeee-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-116">多倍長整数型 (Big Integer)</span><span class="sxs-lookup"><span data-stu-id="beeee-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-117"><strong>示す dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-118">バイナリ型 (Binary)</span><span class="sxs-lookup"><span data-stu-id="beeee-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-120">ブール型 (Boolean)</span><span class="sxs-lookup"><span data-stu-id="beeee-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-122">バイト型 (Byte)</span><span class="sxs-lookup"><span data-stu-id="beeee-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-124">文字型 (Char)</span><span class="sxs-lookup"><span data-stu-id="beeee-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-126">通貨型 (Currency)</span><span class="sxs-lookup"><span data-stu-id="beeee-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-128">日付/時刻型 (Date/Time)</span><span class="sxs-lookup"><span data-stu-id="beeee-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-130">10 進型 (Decimal)</span><span class="sxs-lookup"><span data-stu-id="beeee-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-132">倍精度浮動小数点型 (Double)</span><span class="sxs-lookup"><span data-stu-id="beeee-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-134">浮動小数点型 (Float)</span><span class="sxs-lookup"><span data-stu-id="beeee-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-135"><strong>データと</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-136">GUID 型 (GUID)</span><span class="sxs-lookup"><span data-stu-id="beeee-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-138">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="beeee-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-140">Long 型 (Long)</span><span class="sxs-lookup"><span data-stu-id="beeee-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-142">ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)</span><span class="sxs-lookup"><span data-stu-id="beeee-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-144">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="beeee-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-146">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="beeee-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-148">単精度浮動小数点型 (Single)</span><span class="sxs-lookup"><span data-stu-id="beeee-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-150">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="beeee-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-152">時刻型 (Time)</span><span class="sxs-lookup"><span data-stu-id="beeee-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="beeee-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-154">タイムスタンプ型 (TimeStamp)</span><span class="sxs-lookup"><span data-stu-id="beeee-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="beeee-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="beeee-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="beeee-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="beeee-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="beeee-157">新しい **Field** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="beeee-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

