---
title: Parameter.Type プロパティ (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 294d61ba964958d7933a68919df940cb7501ec0d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927033"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="95e49-102">Parameter.Type プロパティ (DAO)</span><span class="sxs-lookup"><span data-stu-id="95e49-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="95e49-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="95e49-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95e49-p101">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 ( **Integer** ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95e49-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e49-106">構文</span><span class="sxs-lookup"><span data-stu-id="95e49-106">Syntax</span></span>

<span data-ttu-id="95e49-107">*式*です。タイプ</span><span class="sxs-lookup"><span data-stu-id="95e49-107">*expression* .Type</span></span>

<span data-ttu-id="95e49-108">\*式\***パラメーター**オブジェクトを表す変数です。</span><span class="sxs-lookup"><span data-stu-id="95e49-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e49-109">注釈</span><span class="sxs-lookup"><span data-stu-id="95e49-109">Remarks</span></span>

<span data-ttu-id="95e49-p102">設定値または戻り値は、操作の種類またはデータ型を示す定数です。Microsoft Access ワークスペース内の **[Parameter](parameter-object-dao.md)** オブジェクトでは、このプロパティは値の取得のみ可能です。</span><span class="sxs-lookup"><span data-stu-id="95e49-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="95e49-112">次の表は、 **Parameter** オブジェクトで使用可能な設定値および戻り値を示しています。</span><span class="sxs-lookup"><span data-stu-id="95e49-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95e49-113">定数</span><span class="sxs-lookup"><span data-stu-id="95e49-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="95e49-114">説明</span><span class="sxs-lookup"><span data-stu-id="95e49-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95e49-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-116">多倍長整数型 (Big Integer)</span><span class="sxs-lookup"><span data-stu-id="95e49-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-117"><strong>示す dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-118">バイナリ型 (Binary)</span><span class="sxs-lookup"><span data-stu-id="95e49-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-120">ブール型 (Boolean)</span><span class="sxs-lookup"><span data-stu-id="95e49-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-122">バイト型 (Byte)</span><span class="sxs-lookup"><span data-stu-id="95e49-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-124">文字型 (Char)</span><span class="sxs-lookup"><span data-stu-id="95e49-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-126">通貨型 (Currency)</span><span class="sxs-lookup"><span data-stu-id="95e49-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-128">日付/時刻型 (Date/Time)</span><span class="sxs-lookup"><span data-stu-id="95e49-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-130">10 進型 (Decimal)</span><span class="sxs-lookup"><span data-stu-id="95e49-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-132">倍精度浮動小数点型 (Double)</span><span class="sxs-lookup"><span data-stu-id="95e49-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-134">浮動小数点型 (Float)</span><span class="sxs-lookup"><span data-stu-id="95e49-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-135"><strong>データと</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-136">GUID 型 (GUID)</span><span class="sxs-lookup"><span data-stu-id="95e49-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-138">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="95e49-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-140">Long 型 (Long)</span><span class="sxs-lookup"><span data-stu-id="95e49-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-142">ロング バイナリ型 (Long Binary) - OLE オブジェクト型 (OLE Object)</span><span class="sxs-lookup"><span data-stu-id="95e49-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-144">メモ型 (Memo)</span><span class="sxs-lookup"><span data-stu-id="95e49-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-146">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="95e49-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-148">単精度浮動小数点型 (Single)</span><span class="sxs-lookup"><span data-stu-id="95e49-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-150">テキスト型 (Text)</span><span class="sxs-lookup"><span data-stu-id="95e49-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-152">時刻型 (Time)</span><span class="sxs-lookup"><span data-stu-id="95e49-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95e49-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-154">タイムスタンプ型 (TimeStamp)</span><span class="sxs-lookup"><span data-stu-id="95e49-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95e49-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="95e49-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="95e49-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="95e49-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="95e49-157">新しい **Field** オブジェクト、 **Parameter** オブジェクト、または **Property** オブジェクトを **[Index](index-object-dao.md)** オブジェクト、 **QueryDef** オブジェクト、 **Recordset** オブジェクト、または **TableDef** オブジェクトのコレクションに追加するときに、基になるデータベースが新しいオブジェクトに指定されているデータ型をサポートしていない場合、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="95e49-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

